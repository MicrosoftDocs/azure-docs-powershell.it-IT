---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194590"
---
# <span data-ttu-id="c6ac7-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="c6ac7-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="c6ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ac7-103">Recupera informazioni sui dettagli della sincronizzazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="c6ac7-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="c6ac7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6ac7-104">SYNTAX</span></span>

### <span data-ttu-id="c6ac7-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6ac7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6ac7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ac7-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6ac7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6ac7-107">DESCRIPTION</span></span>
<span data-ttu-id="c6ac7-108">Il cmdlet **Get-AzDataShareSynchronizationDetail** fornisce i dettagli della sincronizzazione avviata per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="c6ac7-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="c6ac7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6ac7-109">EXAMPLES</span></span>

### <span data-ttu-id="c6ac7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6ac7-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="c6ac7-111">Questo comando fornisce informazioni sui dettagli della sincronizzazione di tutti i set di dati corrispondenti all'ID di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c6ac7-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="c6ac7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6ac7-112">PARAMETERS</span></span>

### <span data-ttu-id="c6ac7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6ac7-113">-AccountName</span></span>
<span data-ttu-id="c6ac7-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c6ac7-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ac7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ac7-115">-DefaultProfile</span></span>
<span data-ttu-id="c6ac7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6ac7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6ac7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ac7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c6ac7-118">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c6ac7-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ac7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6ac7-119">-ResourceId</span></span>
<span data-ttu-id="c6ac7-120">ID risorsa condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c6ac7-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6ac7-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c6ac7-121">-ShareName</span></span>
<span data-ttu-id="c6ac7-122">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c6ac7-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ac7-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="c6ac7-123">-SynchronizationId</span></span>
<span data-ttu-id="c6ac7-124">ID sincronizzazione della sincronizzazione della condivisione</span><span class="sxs-lookup"><span data-stu-id="c6ac7-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="c6ac7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ac7-125">CommonParameters</span></span>
<span data-ttu-id="c6ac7-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ac7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ac7-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6ac7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ac7-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6ac7-128">INPUTS</span></span>

### <span data-ttu-id="c6ac7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c6ac7-129">System.String</span></span>

## <span data-ttu-id="c6ac7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6ac7-130">OUTPUTS</span></span>

### <span data-ttu-id="c6ac7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="c6ac7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="c6ac7-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6ac7-132">NOTES</span></span>

## <span data-ttu-id="c6ac7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6ac7-133">RELATED LINKS</span></span>
