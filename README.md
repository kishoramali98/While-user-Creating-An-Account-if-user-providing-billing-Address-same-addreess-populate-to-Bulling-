# While-user-Creating-An-Account-if-user-providing-billing-Address-same-addreess-populate-to-Bulling-
While user Creating An Account if user providing billing Address  same address populate to Bulling Address field 
trigger ShippingAddressUpdate on Account(before insert)
{
 if(trigger.isbefore && trigger.isinsert)
{
  for(Account acc:trigger.new)
      {
       if(acc.shippingCity ==null)
        {
           acc.shippingCity=acc.billingCity;
        }


        if(acc.ShippingCountry==null)
         {
           acc.shippingCountry==acc.billingCountry;
         }


         if(acc.ShippingState==null)
         {
           acc.shippingCountry==acc.billingstate;
         }
          if(acc.ShippingPastalcode==null)
         {
           acc.shippingCountry==acc.billingpostalcode;
         }
      }
}
}
