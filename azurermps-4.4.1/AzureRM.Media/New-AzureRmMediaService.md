---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687162"
---
# <span data-ttu-id="2e52c-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2e52c-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="2e52c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e52c-102">SYNOPSIS</span></span>
<span data-ttu-id="2e52c-103">Crea un servizio multimediale se il servizio multimediale esiste già, tutte le relative proprietà vengono aggiornate con l'input fornito.</span><span class="sxs-lookup"><span data-stu-id="2e52c-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e52c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e52c-104">SYNTAX</span></span>

### <span data-ttu-id="2e52c-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="2e52c-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e52c-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="2e52c-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e52c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e52c-107">DESCRIPTION</span></span>
<span data-ttu-id="2e52c-108">Il cmdlet **New-AzureRmMediaService** crea un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2e52c-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="2e52c-109">Se il servizio multimediale esiste già, questo cmdlet aggiorna le proprie proprietà.</span><span class="sxs-lookup"><span data-stu-id="2e52c-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="2e52c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e52c-110">EXAMPLES</span></span>

### <span data-ttu-id="2e52c-111">Esempio1: creare un servizio multimediale solo con l'account di archiviazione principale</span><span class="sxs-lookup"><span data-stu-id="2e52c-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="2e52c-112">Questo esempio Mostra come creare un servizio multimediale specificando solo l'account di archiviazione principale.</span><span class="sxs-lookup"><span data-stu-id="2e52c-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="2e52c-113">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e52c-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="2e52c-114">Esempio 2: creare un servizio multimediale con più spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2e52c-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="2e52c-115">Questo esempio Mostra come creare un servizio multimediale con più account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e52c-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="2e52c-116">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e52c-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="2e52c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e52c-117">PARAMETERS</span></span>

### <span data-ttu-id="2e52c-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e52c-118">-AccountName</span></span>
<span data-ttu-id="2e52c-119">Specifica il nome del servizio multimediale creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e52c-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2e52c-120">-Location</span></span>
<span data-ttu-id="2e52c-121">Specifica l'area geografica in cui questo cmdlet crea il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2e52c-121">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e52c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e52c-123">Specifica il nome del gruppo di risorse a cui è assegnato il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2e52c-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-124">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2e52c-124">-StorageAccountId</span></span>
<span data-ttu-id="2e52c-125">Specifica l'account di archiviazione associato all'account del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2e52c-125">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="2e52c-126">-StorageAccounts</span></span>
<span data-ttu-id="2e52c-127">Specifica una matrice di account di archiviazione da associare al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2e52c-127">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e52c-128">-Tags</span></span>
<span data-ttu-id="2e52c-129">Specifica i contrassegni per il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2e52c-129">Specifies tags for the media service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e52c-130">-Confirm</span></span>
<span data-ttu-id="2e52c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e52c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e52c-132">-WhatIf</span></span>
<span data-ttu-id="2e52c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e52c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e52c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e52c-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e52c-135">-DefaultProfile</span></span>
<span data-ttu-id="2e52c-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e52c-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e52c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e52c-137">CommonParameters</span></span>
<span data-ttu-id="2e52c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e52c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e52c-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e52c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e52c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e52c-140">INPUTS</span></span>

## <span data-ttu-id="2e52c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e52c-141">OUTPUTS</span></span>

### <span data-ttu-id="2e52c-142">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="2e52c-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="2e52c-143">Note</span><span class="sxs-lookup"><span data-stu-id="2e52c-143">NOTES</span></span>

## <span data-ttu-id="2e52c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e52c-144">RELATED LINKS</span></span>

[<span data-ttu-id="2e52c-145">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2e52c-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="2e52c-146">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2e52c-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="2e52c-147">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2e52c-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


