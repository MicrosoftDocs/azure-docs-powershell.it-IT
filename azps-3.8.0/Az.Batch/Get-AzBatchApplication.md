---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022098"
---
# <span data-ttu-id="64976-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64976-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="64976-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64976-102">SYNOPSIS</span></span>
<span data-ttu-id="64976-103">Ottiene le informazioni sull'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="64976-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="64976-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64976-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64976-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64976-105">DESCRIPTION</span></span>
<span data-ttu-id="64976-106">Il cmdlet **Get-AzBatchApplication** ottiene le informazioni su un'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="64976-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="64976-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64976-107">EXAMPLES</span></span>

### <span data-ttu-id="64976-108">Esempio 1: visualizzare le applicazioni in un account batch</span><span class="sxs-lookup"><span data-stu-id="64976-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="64976-109">Questo comando Visualizza tutte le applicazioni nell'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="64976-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="64976-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64976-110">PARAMETERS</span></span>

### <span data-ttu-id="64976-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="64976-111">-AccountName</span></span>
<span data-ttu-id="64976-112">Specifica il nome dell'account batch che contiene l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64976-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="64976-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="64976-113">-ApplicationName</span></span>
<span data-ttu-id="64976-114">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64976-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64976-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64976-115">-DefaultProfile</span></span>
<span data-ttu-id="64976-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64976-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64976-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64976-117">-ResourceGroupName</span></span>
<span data-ttu-id="64976-118">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="64976-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64976-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64976-119">CommonParameters</span></span>
<span data-ttu-id="64976-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64976-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64976-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64976-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64976-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64976-122">INPUTS</span></span>

### <span data-ttu-id="64976-123">System. String</span><span class="sxs-lookup"><span data-stu-id="64976-123">System.String</span></span>

## <span data-ttu-id="64976-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64976-124">OUTPUTS</span></span>

### <span data-ttu-id="64976-125">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="64976-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="64976-126">Note</span><span class="sxs-lookup"><span data-stu-id="64976-126">NOTES</span></span>

## <span data-ttu-id="64976-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64976-127">RELATED LINKS</span></span>

[<span data-ttu-id="64976-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="64976-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="64976-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64976-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="64976-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="64976-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="64976-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64976-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="64976-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="64976-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="64976-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="64976-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


