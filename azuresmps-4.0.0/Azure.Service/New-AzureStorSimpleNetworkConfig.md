---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023473"
---
# <span data-ttu-id="27c27-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="27c27-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="27c27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27c27-102">SYNOPSIS</span></span>
<span data-ttu-id="27c27-103">Prepara un oggetto di configurazione della rete.</span><span class="sxs-lookup"><span data-stu-id="27c27-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="27c27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27c27-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="27c27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27c27-105">DESCRIPTION</span></span>
<span data-ttu-id="27c27-106">Il cmdlet **New-AzureStorSimpleNetworkConfig** prepara un oggetto di configurazione della rete per passare al cmdlet **set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="27c27-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="27c27-107">Imposta il parametro *Controller0IPAddress* e il parametro *Controller1IPAddress* solo nell'interfaccia data0.</span><span class="sxs-lookup"><span data-stu-id="27c27-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="27c27-108">DATA0 supporta solo tre impostazioni: *Controller0IPAddress* , *Controller1IPAdress* e *EnableIscsi*.</span><span class="sxs-lookup"><span data-stu-id="27c27-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="27c27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27c27-109">EXAMPLES</span></span>

### <span data-ttu-id="27c27-110">Esempio 1: configurare un'interfaccia DATA0</span><span class="sxs-lookup"><span data-stu-id="27c27-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="27c27-111">Questo comando crea la configurazione di rete per l'interfaccia data0.</span><span class="sxs-lookup"><span data-stu-id="27c27-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="27c27-112">Questo comando specifica i parametri *Controller0IPv4Address* , *Controller1IPv4Address* e *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="27c27-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="27c27-113">Questo cmdlet può configurare DATA0 solo per questi tre parametri.</span><span class="sxs-lookup"><span data-stu-id="27c27-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="27c27-114">Esempio 2: configurare un'interfaccia diversa da DATA0</span><span class="sxs-lookup"><span data-stu-id="27c27-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="27c27-115">Questo comando configura l'interfaccia Data1.</span><span class="sxs-lookup"><span data-stu-id="27c27-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="27c27-116">Esempio 3: modificare una configurazione per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="27c27-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="27c27-117">Il primo comando crea una configurazione di rete per l'interfaccia data0.</span><span class="sxs-lookup"><span data-stu-id="27c27-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="27c27-118">Questo comando specifica i parametri *Controller0IPv4Address* , *Controller1IPv4Address* e *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="27c27-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="27c27-119">Il comando Archivia il risultato nella variabile $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="27c27-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="27c27-120">Il secondo comando usa il cmdlet **Get-AzureStorSimpleDevice** e il cmdlet **Where-Object** core per ottenere un dispositivo StorSimple online e lo archivia nella variabile $OnlineDevice.</span><span class="sxs-lookup"><span data-stu-id="27c27-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="27c27-121">Il comando Final modifica la configurazione per il dispositivo con l'ID del dispositivo specificato usando il cmdlet **set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="27c27-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="27c27-122">Il comando usa l'oggetto Configuration che il cmdlet corrente ha creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="27c27-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="27c27-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27c27-123">PARAMETERS</span></span>

### <span data-ttu-id="27c27-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="27c27-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="27c27-125">Specifica l'indirizzo IPv4 per il controller 0.</span><span class="sxs-lookup"><span data-stu-id="27c27-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="27c27-126">Specifica questo parametro solo per l'interfaccia data0.</span><span class="sxs-lookup"><span data-stu-id="27c27-126">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="27c27-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="27c27-128">Specifica l'indirizzo IPv4 per il controller 1.</span><span class="sxs-lookup"><span data-stu-id="27c27-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="27c27-129">Specifica questo parametro solo per l'interfaccia data0.</span><span class="sxs-lookup"><span data-stu-id="27c27-129">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="27c27-130">-EnableCloud</span></span>
<span data-ttu-id="27c27-131">Indica se abilitare il cloud all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="27c27-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="27c27-132">-EnableIscsi</span></span>
<span data-ttu-id="27c27-133">Indica se abilitare Internet SCSI (ISCSI) per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="27c27-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="27c27-134">-InterfaceAlias</span></span>
<span data-ttu-id="27c27-135">Specifica l'alias di interfaccia dell'interfaccia per cui questo cmdlet fornisce le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="27c27-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="27c27-136">I valori validi sono da DATA0 a data5.</span><span class="sxs-lookup"><span data-stu-id="27c27-136">Valid values are from Data0 to Data5.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-137">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="27c27-137">-IPv4Address</span></span>
<span data-ttu-id="27c27-138">Specifica l'indirizzo IPv4 per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="27c27-138">Specifies the IPv4 address for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="27c27-139">-IPv4Gateway</span></span>
<span data-ttu-id="27c27-140">Specifica l'indirizzo IPv4 di un gateway.</span><span class="sxs-lookup"><span data-stu-id="27c27-140">Specifies the IPv4 address of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="27c27-141">-IPv4Netmask</span></span>
<span data-ttu-id="27c27-142">Specifica la netmask IPv4 per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="27c27-142">Specifies the IPv4 netmask for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="27c27-143">-IPv6Gateway</span></span>
<span data-ttu-id="27c27-144">Specifica il gateway IPv6 per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="27c27-144">Specifies the IPv6 gateway for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="27c27-145">-IPv6Prefix</span></span>
<span data-ttu-id="27c27-146">Specifica il prefisso IPv6 per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="27c27-146">Specifies the IPv6 prefix for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="27c27-147">-Profile</span></span>
<span data-ttu-id="27c27-148">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="27c27-148">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c27-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c27-149">CommonParameters</span></span>
<span data-ttu-id="27c27-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c27-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c27-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c27-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c27-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27c27-152">INPUTS</span></span>

### <span data-ttu-id="27c27-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="27c27-153">None</span></span>

## <span data-ttu-id="27c27-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27c27-154">OUTPUTS</span></span>

### <span data-ttu-id="27c27-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="27c27-155">NetworkConfig</span></span>
<span data-ttu-id="27c27-156">Questo cmdlet restituisce un oggetto NetworkConfig che contiene le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="27c27-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="27c27-157">**IsIscsiEnabled** ( **booleano** )</span><span class="sxs-lookup"><span data-stu-id="27c27-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="27c27-158">**IsCloudEnabled** ( **booleano** )</span><span class="sxs-lookup"><span data-stu-id="27c27-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="27c27-159">**Controller0IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="27c27-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="27c27-160">**Controller1IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="27c27-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="27c27-161">**IPv6Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="27c27-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="27c27-162">**IPv4Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="27c27-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="27c27-163">**IndirizzoIPv4** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="27c27-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="27c27-164">**IPv6Prefix** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="27c27-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="27c27-165">**IPv4Netmask** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="27c27-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="27c27-166">**InterfaceAlias** ( **NetInterfaceId** )</span><span class="sxs-lookup"><span data-stu-id="27c27-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="27c27-167">Note</span><span class="sxs-lookup"><span data-stu-id="27c27-167">NOTES</span></span>

## <span data-ttu-id="27c27-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27c27-168">RELATED LINKS</span></span>

[<span data-ttu-id="27c27-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="27c27-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="27c27-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="27c27-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


