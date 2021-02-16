---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183086"
---
# <span data-ttu-id="2829b-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="2829b-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="2829b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2829b-102">SYNOPSIS</span></span>
<span data-ttu-id="2829b-103">Questo comando crea un endpoint cloud di Azure File Sync in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2829b-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="2829b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2829b-104">SYNTAX</span></span>

### <span data-ttu-id="2829b-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="2829b-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2829b-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2829b-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2829b-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2829b-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2829b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2829b-108">DESCRIPTION</span></span>
<span data-ttu-id="2829b-109">Questo comando crea un endpoint cloud di Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="2829b-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="2829b-110">Un endpoint cloud è un riferimento a una condivisione file di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="2829b-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="2829b-111">Rappresenta la condivisione file e la definisce come partecipazione alla sincronizzazione di tutti i file che fanno parte del gruppo di sincronizzazione in cui è stato creato l'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="2829b-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="2829b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2829b-112">EXAMPLES</span></span>

### <span data-ttu-id="2829b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2829b-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="2829b-114">Un endpoint cloud è un membro integrale di un gruppo di sincronizzazione, in questo esempio ne viene creato uno all'interno di un gruppo di sincronizzazione esistente denominato "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="2829b-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="2829b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2829b-115">PARAMETERS</span></span>

### <span data-ttu-id="2829b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2829b-116">-AsJob</span></span>
<span data-ttu-id="2829b-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2829b-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="2829b-118">-AzureFileShareName</span></span>
<span data-ttu-id="2829b-119">Nome condivisione account di archiviazione (nome condivisione file di Azure)</span><span class="sxs-lookup"><span data-stu-id="2829b-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2829b-120">-DefaultProfile</span></span>
<span data-ttu-id="2829b-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2829b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2829b-122">-Name</span></span>
<span data-ttu-id="2829b-123">Nome dell'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="2829b-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="2829b-124">Una volta creato tramite il portale di Azure, il nome viene impostato sul nome della condivisione file di Azure a cui fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="2829b-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2829b-125">-ParentObject</span></span>
<span data-ttu-id="2829b-126">Oggetto SyncGroup, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="2829b-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2829b-127">-ParentResourceId</span></span>
<span data-ttu-id="2829b-128">ID risorsa padre SyncGroup</span><span class="sxs-lookup"><span data-stu-id="2829b-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2829b-129">-ResourceGroupName</span></span>
<span data-ttu-id="2829b-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2829b-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2829b-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="2829b-132">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2829b-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="2829b-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="2829b-134">ID tenant account di archiviazione (ID directory aziendale)</span><span class="sxs-lookup"><span data-stu-id="2829b-134">Storage Account Tenant Id (Company Directory Id)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2829b-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="2829b-136">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2829b-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2829b-137">-SyncGroupName</span></span>
<span data-ttu-id="2829b-138">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2829b-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2829b-139">-Confirm</span></span>
<span data-ttu-id="2829b-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2829b-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2829b-141">-WhatIf</span></span>
<span data-ttu-id="2829b-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2829b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2829b-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2829b-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2829b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2829b-144">CommonParameters</span></span>
<span data-ttu-id="2829b-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2829b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2829b-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2829b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2829b-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="2829b-147">INPUTS</span></span>

### <span data-ttu-id="2829b-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2829b-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="2829b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2829b-149">System.String</span></span>

## <span data-ttu-id="2829b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2829b-150">OUTPUTS</span></span>

### <span data-ttu-id="2829b-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="2829b-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="2829b-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="2829b-152">NOTES</span></span>

## <span data-ttu-id="2829b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2829b-153">RELATED LINKS</span></span>
