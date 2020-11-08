---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023734"
---
# <span data-ttu-id="d57b9-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d57b9-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="d57b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d57b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d57b9-103">Avvia un'operazione di failover dei gruppi di contenitori di volumi.</span><span class="sxs-lookup"><span data-stu-id="d57b9-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="d57b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d57b9-104">SYNTAX</span></span>

### <span data-ttu-id="d57b9-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d57b9-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d57b9-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="d57b9-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d57b9-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="d57b9-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d57b9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d57b9-108">DESCRIPTION</span></span>
<span data-ttu-id="d57b9-109">Il cmdlet **Start-AzureStorSimpleDeviceFailoverJob** avvia un'operazione di failover di uno o più gruppi di contenitori di volumi da un dispositivo a un altro.</span><span class="sxs-lookup"><span data-stu-id="d57b9-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="d57b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d57b9-110">EXAMPLES</span></span>

### <span data-ttu-id="d57b9-111">Esempio 1: avviare un processo di failover per un dispositivo denominato e un dispositivo di destinazione denominato</span><span class="sxs-lookup"><span data-stu-id="d57b9-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="d57b9-112">Questo comando ottiene i contenitori del volume di failover per il dispositivo denominato ChewD_App7 usando il cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** .</span><span class="sxs-lookup"><span data-stu-id="d57b9-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="d57b9-113">Il comando passa i risultati al cmdlet **Where-Object** , che elimina i contenitori che hanno un valore diverso da $true per la proprietà **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="d57b9-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="d57b9-114">Per altre informazioni, digitare `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="d57b9-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="d57b9-115">Il cmdlet corrente avvia i processi di failover per i contenitori del volume di failover rimanenti.</span><span class="sxs-lookup"><span data-stu-id="d57b9-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="d57b9-116">Il comando specifica il nome del dispositivo e il nome del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d57b9-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="d57b9-117">Il comando restituisce l'ID istanza del processo che viene avviato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d57b9-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="d57b9-118">Esempio 2: avviare un processo di failover per un dispositivo e un dispositivo di destinazione specificato da ID</span><span class="sxs-lookup"><span data-stu-id="d57b9-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="d57b9-119">Questo comando ottiene i contenitori del volume di failover per il dispositivo denominato ChewD_App7 tramite **Get-AzureStorSimpleFailoverVolumeContainers**.</span><span class="sxs-lookup"><span data-stu-id="d57b9-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="d57b9-120">Il comando passa i risultati a **Where-Object** , che elimina i containers che hanno un valore diverso da $true per la proprietà **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="d57b9-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="d57b9-121">Il cmdlet passa i risultati al cmdlet **Select-Object** , che seleziona il primo oggetto da passare al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d57b9-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="d57b9-122">Per altre informazioni, digitare `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="d57b9-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="d57b9-123">Il cmdlet corrente avvia i processi di failover per il contenitore del volume di failover selezionato.</span><span class="sxs-lookup"><span data-stu-id="d57b9-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="d57b9-124">Il comando specifica l'ID del dispositivo e l'ID del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d57b9-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="d57b9-125">Il comando restituisce l'ID istanza del processo che viene avviato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d57b9-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="d57b9-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d57b9-126">PARAMETERS</span></span>

### <span data-ttu-id="d57b9-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d57b9-127">-DeviceId</span></span>
<span data-ttu-id="d57b9-128">Specifica l'ID istanza del dispositivo StorSimple in cui sono presenti i gruppi di contenitori del volume.</span><span class="sxs-lookup"><span data-stu-id="d57b9-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="d57b9-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d57b9-129">-DeviceName</span></span>
<span data-ttu-id="d57b9-130">Specifica il nome del dispositivo StorSimple in cui sono presenti i gruppi di contenitori del volume.</span><span class="sxs-lookup"><span data-stu-id="d57b9-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="d57b9-131">-Force</span><span class="sxs-lookup"><span data-stu-id="d57b9-131">-Force</span></span>
<span data-ttu-id="d57b9-132">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d57b9-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57b9-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="d57b9-133">-Profile</span></span>
<span data-ttu-id="d57b9-134">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="d57b9-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d57b9-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="d57b9-135">-TargetDeviceId</span></span>
<span data-ttu-id="d57b9-136">Specifica l'ID istanza del dispositivo StorSimple a cui il cmdlet non riesce sui gruppi di contenitori del volume.</span><span class="sxs-lookup"><span data-stu-id="d57b9-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="d57b9-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="d57b9-137">-TargetDeviceName</span></span>
<span data-ttu-id="d57b9-138">Specifica il nome del dispositivo StorSimple a cui questo cmdlet ha esito negativo sui gruppi di contenitori del volume.</span><span class="sxs-lookup"><span data-stu-id="d57b9-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="d57b9-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="d57b9-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="d57b9-140">Specifica l'elenco dei gruppi di contenitori di volumi a cui il cmdlet esegue il failover su un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d57b9-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57b9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57b9-141">CommonParameters</span></span>
<span data-ttu-id="d57b9-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57b9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57b9-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57b9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57b9-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d57b9-144">INPUTS</span></span>

### <span data-ttu-id="d57b9-145">Elenco\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="d57b9-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="d57b9-146">È possibile reindirizzare un elenco di gruppi di contenitori di volumi a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d57b9-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="d57b9-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d57b9-147">OUTPUTS</span></span>

### <span data-ttu-id="d57b9-148">Stringa</span><span class="sxs-lookup"><span data-stu-id="d57b9-148">String</span></span>

## <span data-ttu-id="d57b9-149">Note</span><span class="sxs-lookup"><span data-stu-id="d57b9-149">NOTES</span></span>

## <span data-ttu-id="d57b9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d57b9-150">RELATED LINKS</span></span>

[<span data-ttu-id="d57b9-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="d57b9-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


