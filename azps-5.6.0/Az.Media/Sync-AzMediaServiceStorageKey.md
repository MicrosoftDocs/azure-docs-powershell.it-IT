---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 75e83c3d861bfbe579634da0ee136f564be43ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982974"
---
# <span data-ttu-id="249a0-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="249a0-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="249a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="249a0-102">SYNOPSIS</span></span>
<span data-ttu-id="249a0-103">Sincronizza le chiavi dell'account di archiviazione per un account di archiviazione associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="249a0-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="249a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="249a0-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="249a0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="249a0-105">DESCRIPTION</span></span>
<span data-ttu-id="249a0-106">Il cmdlet **Sync-AzMediaServiceStorageKey** sincronizza le chiavi dell'account di archiviazione per un account di archiviazione associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="249a0-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="249a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="249a0-107">EXAMPLES</span></span>

### <span data-ttu-id="249a0-108">Esempio 1: Sincronizzare le chiavi dell'account di archiviazione per un account di archiviazione associato al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="249a0-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="249a0-109">Il primo comando usa il cmdlet Get-AzStorageAccount per ottenere l'account di archiviazione denominato Storage135 che appartiene a ResourceGroup001 e archivia il risultato nella variabile $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="249a0-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="249a0-110">Il secondo comando sincronizza le chiavi dell'account di archiviazione per il servizio multimediale denominato MediaService001 usando la **proprietà Id** contenuta nella $StorageAccount variabile.</span><span class="sxs-lookup"><span data-stu-id="249a0-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="249a0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="249a0-111">PARAMETERS</span></span>

### <span data-ttu-id="249a0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="249a0-112">-AccountName</span></span>
<span data-ttu-id="249a0-113">Specifica il nome del servizio multimediale sincronizzato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249a0-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="249a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="249a0-114">-DefaultProfile</span></span>
<span data-ttu-id="249a0-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="249a0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="249a0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="249a0-116">-ResourceGroupName</span></span>
<span data-ttu-id="249a0-117">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="249a0-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="249a0-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="249a0-118">-StorageAccountId</span></span>
<span data-ttu-id="249a0-119">Specifica l'ID account di archiviazione associato all'account del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="249a0-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249a0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="249a0-120">-Confirm</span></span>
<span data-ttu-id="249a0-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="249a0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="249a0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="249a0-122">-WhatIf</span></span>
<span data-ttu-id="249a0-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="249a0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="249a0-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="249a0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="249a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="249a0-125">CommonParameters</span></span>
<span data-ttu-id="249a0-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="249a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="249a0-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="249a0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="249a0-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="249a0-128">INPUTS</span></span>

### <span data-ttu-id="249a0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="249a0-129">System.String</span></span>

## <span data-ttu-id="249a0-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="249a0-130">OUTPUTS</span></span>

### <span data-ttu-id="249a0-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="249a0-131">System.Boolean</span></span>

## <span data-ttu-id="249a0-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="249a0-132">NOTES</span></span>

## <span data-ttu-id="249a0-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="249a0-133">RELATED LINKS</span></span>
