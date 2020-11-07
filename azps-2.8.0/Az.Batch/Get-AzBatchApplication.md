---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: fa08214e141d035e7c449e591f6a4820f758b48c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675663"
---
# <span data-ttu-id="61065-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61065-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="61065-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61065-102">SYNOPSIS</span></span>
<span data-ttu-id="61065-103">Ottiene le informazioni sull'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="61065-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="61065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61065-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61065-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61065-105">DESCRIPTION</span></span>
<span data-ttu-id="61065-106">Il cmdlet **Get-AzBatchApplication** ottiene le informazioni su un'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="61065-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="61065-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61065-107">EXAMPLES</span></span>

### <span data-ttu-id="61065-108">Esempio 1: visualizzare le applicazioni in un account batch</span><span class="sxs-lookup"><span data-stu-id="61065-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="61065-109">Questo comando Visualizza tutte le applicazioni nell'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="61065-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="61065-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61065-110">PARAMETERS</span></span>

### <span data-ttu-id="61065-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61065-111">-AccountName</span></span>
<span data-ttu-id="61065-112">Specifica il nome dell'account batch che contiene l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61065-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="61065-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="61065-113">-ApplicationId</span></span>
<span data-ttu-id="61065-114">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61065-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61065-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61065-115">-DefaultProfile</span></span>
<span data-ttu-id="61065-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61065-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61065-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61065-117">-ResourceGroupName</span></span>
<span data-ttu-id="61065-118">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="61065-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="61065-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61065-119">CommonParameters</span></span>
<span data-ttu-id="61065-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61065-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61065-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61065-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61065-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61065-122">INPUTS</span></span>

### <span data-ttu-id="61065-123">System. String</span><span class="sxs-lookup"><span data-stu-id="61065-123">System.String</span></span>

## <span data-ttu-id="61065-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61065-124">OUTPUTS</span></span>

### <span data-ttu-id="61065-125">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="61065-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="61065-126">Note</span><span class="sxs-lookup"><span data-stu-id="61065-126">NOTES</span></span>

## <span data-ttu-id="61065-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61065-127">RELATED LINKS</span></span>

[<span data-ttu-id="61065-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="61065-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="61065-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61065-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="61065-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="61065-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="61065-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61065-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="61065-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="61065-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="61065-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="61065-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


