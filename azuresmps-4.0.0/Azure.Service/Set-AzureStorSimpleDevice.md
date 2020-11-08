---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: AE8E6778-1299-4EC7-BFE0-3FB464AA7BB4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7bea5cbf2b5e10c85aaafa43203c207193040464
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023711"
---
# <span data-ttu-id="dc91c-101">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="dc91c-101">Set-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="dc91c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc91c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc91c-103">Modifica la configurazione del dispositivo per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc91c-103">Changes the device configuration for a device.</span></span>

## <span data-ttu-id="dc91c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc91c-104">SYNTAX</span></span>

### <span data-ttu-id="dc91c-105">IdentifyByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc91c-105">IdentifyByName (Default)</span></span>
```
Set-AzureStorSimpleDevice -DeviceName <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc91c-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="dc91c-106">IdentifyById</span></span>
```
Set-AzureStorSimpleDevice -DeviceId <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc91c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc91c-107">DESCRIPTION</span></span>
<span data-ttu-id="dc91c-108">Il cmdlet **set-AzureStorSimpleDevice** modifica la configurazione del dispositivo per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc91c-108">The **Set-AzureStorSimpleDevice** cmdlet changes the device configuration for a device.</span></span>
<span data-ttu-id="dc91c-109">Se si sta configurando un dispositivo per la prima volta, è necessario specificare i parametri *TimeZone* , *SecondaryDnsServer* e *StorSimpleNetworkConfig* .</span><span class="sxs-lookup"><span data-stu-id="dc91c-109">If you are setting up a device for the first time, you must specify the *TimeZone* , *SecondaryDnsServer* , and *StorSimpleNetworkConfig* parameters.</span></span>
<span data-ttu-id="dc91c-110">Devi includere la configurazione di rete per DATA0 con Controller0 e Controller1 e gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="dc91c-110">You must include network configuration for Data0 with controller0 and controller1 and IP addresses.</span></span>
<span data-ttu-id="dc91c-111">Per configurare il dispositivo per la prima volta, è necessario che sia presente almeno un'interfaccia di rete con accesso Internet SCSI (ISCSI).</span><span class="sxs-lookup"><span data-stu-id="dc91c-111">There must be at least one Internet SCSI (ISCSI)-enabled network interface to configure the device for the first time.</span></span>

## <span data-ttu-id="dc91c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc91c-112">EXAMPLES</span></span>

### <span data-ttu-id="dc91c-113">Esempio 1: modificare la configurazione di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="dc91c-113">Example 1: Modify the configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="dc91c-114">Il primo comando crea una configurazione di rete per l'interfaccia data0.</span><span class="sxs-lookup"><span data-stu-id="dc91c-114">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="dc91c-115">Questo comando specifica i parametri *Controller0IPv4Address* , *Controller1IPv4Address* e *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="dc91c-115">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="dc91c-116">Il comando Archivia il risultato nella variabile $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="dc91c-116">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="dc91c-117">Il secondo comando usa la classe **System. TimeZoneInfo** .NET e la sintassi standard per ottenere il fuso orario Pacifico standard e archivia tale oggetto nella variabile $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="dc91c-117">The second command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="dc91c-118">Il terzo comando usa il cmdlet **Get-AzureStorSimpleDevice** e il cmdlet **Where-Object** core per ottenere un dispositivo StorSimple online e quindi lo archivia nella variabile $OnlineDevice.</span><span class="sxs-lookup"><span data-stu-id="dc91c-118">The third command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="dc91c-119">Il comando Final modifica la configurazione per il dispositivo con l'ID del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="dc91c-119">The final command modifies the configuration for the device that has the specified device ID.</span></span>
<span data-ttu-id="dc91c-120">Il comando usa l'oggetto Configuration che il cmdlet corrente ha creato nel primo comando.</span><span class="sxs-lookup"><span data-stu-id="dc91c-120">The command uses the configuration object that the current cmdlet created in the first command.</span></span>
<span data-ttu-id="dc91c-121">Il comando usa il fuso orario archiviato in $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="dc91c-121">The command uses the time zone stored in $TimeZoneInfo.</span></span>

### <span data-ttu-id="dc91c-122">Esempio 2: eseguire il piping dell'oggetto Configuration per modificare un dispositivo</span><span class="sxs-lookup"><span data-stu-id="dc91c-122">Example 2: Pipe the configuration object to modify a device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 
VERBOSE: ClientRequestId: fa2f5000-169c-4feb-abbf-23f4b5c837fa_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: fae6a491-919c-44b2-93e0-0c51f202c24b_PS
VERBOSE: ClientRequestId: e1803427-a097-4d58-ab7d-14a4c39fd768_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 9e796c3d-3100-46ab-9a09-0e10c73a296f_PS
VERBOSE: ClientRequestId: 5b4cad96-31f4-4d07-a278-df5af3e06ad4_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 9061f7df-144f-4f30-858c-045d882ca392_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 2ed2fa9b-8459-4cd6-9a61-5fc25ced2815_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="dc91c-123">Questo esempio esegue lo stesso aggiornamento della configurazione del primo esempio, con la differenza che il comando finale passa l'oggetto configurazione di rete al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc91c-123">This example does the same configuration update as the first example, except that the final command passes the network configuration object to the current cmdlet by using the pipeline operator.</span></span>

### <span data-ttu-id="dc91c-124">Esempio 3: reindirizzare l'oggetto fuso orario per modificare un dispositivo</span><span class="sxs-lookup"><span data-stu-id="dc91c-124">Example 3: Pipe the time zone object to modify a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: cfc3f3c7-a8b6-462b-96f4-124050b736fe_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 6017b76f-a771-4bf8-901e-14876e0f9962_PS
VERBOSE: ClientRequestId: 59a9275c-9005-4e8a-b68b-efa1e6c27d47_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 08e5142a-b038-4607-8690-0c5a8b948352_PS
VERBOSE: ClientRequestId: 218af244-b8f4-4a4b-817e-8f67e1323f03_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: fbd1f32d-1d74-432e-9dc0-90b46674884a_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 981cb941-252c-4898-ba9f-f19e5b8bcaa4_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="dc91c-125">Questo esempio esegue lo stesso aggiornamento della configurazione del primo esempio, tranne per il fatto che il comando finale passa l'oggetto fuso orario al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc91c-125">This example does the same configuration update as the first example, except that the final command passes the time zone object to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="dc91c-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc91c-126">PARAMETERS</span></span>

### <span data-ttu-id="dc91c-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="dc91c-127">-DeviceId</span></span>
<span data-ttu-id="dc91c-128">Specifica l'ID istanza del dispositivo StorSimple da configurare.</span><span class="sxs-lookup"><span data-stu-id="dc91c-128">Specifies the instance ID of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc91c-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dc91c-129">-DeviceName</span></span>
<span data-ttu-id="dc91c-130">Specifica il nome descrittivo del dispositivo StorSimple da configurare.</span><span class="sxs-lookup"><span data-stu-id="dc91c-130">Specifies the friendly name of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc91c-131">-NewName</span><span class="sxs-lookup"><span data-stu-id="dc91c-131">-NewName</span></span>
<span data-ttu-id="dc91c-132">Specifica il nuovo nome descrittivo del dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="dc91c-132">Specifies the new friendly name of the StorSimple device.</span></span>

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

### <span data-ttu-id="dc91c-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="dc91c-133">-Profile</span></span>
<span data-ttu-id="dc91c-134">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="dc91c-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="dc91c-135">-SecondaryDnsServer</span><span class="sxs-lookup"><span data-stu-id="dc91c-135">-SecondaryDnsServer</span></span>
<span data-ttu-id="dc91c-136">Specifica un server DNS secondario per il dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="dc91c-136">Specifies a secondary DNS server for the StorSimple device.</span></span>

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

### <span data-ttu-id="dc91c-137">-StorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="dc91c-137">-StorSimpleNetworkConfig</span></span>
<span data-ttu-id="dc91c-138">Specifica una matrice di oggetti di configurazione della rete per le interfacce in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc91c-138">Specifies an array of network configuration objectss for interfaces on a device.</span></span>
<span data-ttu-id="dc91c-139">Per ottenere un oggetto **NetworkConfig** , usa il cmdlet New-AzureStorSimpleNetworkConfig.</span><span class="sxs-lookup"><span data-stu-id="dc91c-139">To obtain a **NetworkConfig** object, use the New-AzureStorSimpleNetworkConfig cmdlet.</span></span>

```yaml
Type: NetworkConfig[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc91c-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="dc91c-140">-TimeZone</span></span>
<span data-ttu-id="dc91c-141">Specifica un fuso orario per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc91c-141">Specifies a time zone for the device.</span></span>
<span data-ttu-id="dc91c-142">Puoi creare un oggetto **TimeZoneInfo** usando il metodo **GetSystemTimeZone ()** .</span><span class="sxs-lookup"><span data-stu-id="dc91c-142">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="dc91c-143">Ad esempio, questo comando crea un oggetto informazioni sul fuso orario per l'ora solare Pacifico: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="dc91c-143">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc91c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc91c-144">CommonParameters</span></span>
<span data-ttu-id="dc91c-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc91c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc91c-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc91c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc91c-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc91c-147">INPUTS</span></span>

### <span data-ttu-id="dc91c-148">NetworkConfig, TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="dc91c-148">NetworkConfig, TimeZoneInfo</span></span>
<span data-ttu-id="dc91c-149">Puoi reindirizzare un oggetto **NetworkConfig** o un **TimeZoneInfo** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc91c-149">You can pipe a **NetworkConfig** object or a **TimeZoneInfo** to this cmdlet.</span></span>

## <span data-ttu-id="dc91c-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc91c-150">OUTPUTS</span></span>

### <span data-ttu-id="dc91c-151">DeviceDetails</span><span class="sxs-lookup"><span data-stu-id="dc91c-151">DeviceDetails</span></span>
<span data-ttu-id="dc91c-152">Questo cmdlet restituisce i dettagli del dispositivo aggiornati per il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc91c-152">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="dc91c-153">Note</span><span class="sxs-lookup"><span data-stu-id="dc91c-153">NOTES</span></span>

## <span data-ttu-id="dc91c-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc91c-154">RELATED LINKS</span></span>

[<span data-ttu-id="dc91c-155">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="dc91c-155">New-AzureStorSimpleNetworkConfig</span></span>](./New-AzureStorSimpleNetworkConfig.md)

[<span data-ttu-id="dc91c-156">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="dc91c-156">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


