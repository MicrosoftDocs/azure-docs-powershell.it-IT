---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: c3320c4b60a91c8a4f4b5c02ab46eb68b2f2d37c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674680"
---
# <span data-ttu-id="b405e-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="b405e-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="b405e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b405e-102">SYNOPSIS</span></span>
<span data-ttu-id="b405e-103">Ottiene informazioni sui dettagli della sincronizzazione per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="b405e-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="b405e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b405e-104">SYNTAX</span></span>

### <span data-ttu-id="b405e-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b405e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b405e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b405e-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b405e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b405e-107">DESCRIPTION</span></span>
<span data-ttu-id="b405e-108">Il cmdlet **Get-AzDataShareSynchronizationDetail** fornisce informazioni dettagliate sulla sincronizzazione avviata per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="b405e-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="b405e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b405e-109">EXAMPLES</span></span>

### <span data-ttu-id="b405e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b405e-110">Example 1</span></span>
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

<span data-ttu-id="b405e-111">Questo comando fornisce informazioni sui dettagli della sincronizzazione di tutti i set di dati corrispondenti all'ID di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b405e-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="b405e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b405e-112">PARAMETERS</span></span>

### <span data-ttu-id="b405e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b405e-113">-AccountName</span></span>
<span data-ttu-id="b405e-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b405e-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b405e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b405e-115">-DefaultProfile</span></span>
<span data-ttu-id="b405e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b405e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b405e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b405e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b405e-118">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b405e-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b405e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b405e-119">-ResourceId</span></span>
<span data-ttu-id="b405e-120">ID risorsa condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b405e-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="b405e-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b405e-121">-ShareName</span></span>
<span data-ttu-id="b405e-122">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b405e-122">Azure data share name</span></span>

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

### <span data-ttu-id="b405e-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="b405e-123">-SynchronizationId</span></span>
<span data-ttu-id="b405e-124">ID sincronizzazione della sincronizzazione delle condivisioni</span><span class="sxs-lookup"><span data-stu-id="b405e-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="b405e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b405e-125">CommonParameters</span></span>
<span data-ttu-id="b405e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b405e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b405e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b405e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b405e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b405e-128">INPUTS</span></span>

### <span data-ttu-id="b405e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b405e-129">System.String</span></span>

## <span data-ttu-id="b405e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b405e-130">OUTPUTS</span></span>

### <span data-ttu-id="b405e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="b405e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="b405e-132">Note</span><span class="sxs-lookup"><span data-stu-id="b405e-132">NOTES</span></span>

## <span data-ttu-id="b405e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b405e-133">RELATED LINKS</span></span>
