---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: e22d3c58072fbabd3f927f6b9065f22422492622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508387"
---
# <span data-ttu-id="c8abb-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c8abb-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="c8abb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8abb-102">SYNOPSIS</span></span>
<span data-ttu-id="c8abb-103">Ottiene le informazioni sull'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="c8abb-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8abb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8abb-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8abb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8abb-105">DESCRIPTION</span></span>
<span data-ttu-id="c8abb-106">Il cmdlet **Get-AzureRmBatchApplication** ottiene le informazioni su un'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="c8abb-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="c8abb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8abb-107">EXAMPLES</span></span>

### <span data-ttu-id="c8abb-108">Esempio 1: visualizzare le applicazioni in un account batch</span><span class="sxs-lookup"><span data-stu-id="c8abb-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="c8abb-109">Questo comando Visualizza tutte le applicazioni nell'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="c8abb-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="c8abb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8abb-110">PARAMETERS</span></span>

### <span data-ttu-id="c8abb-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c8abb-111">-AccountName</span></span>
<span data-ttu-id="c8abb-112">Specifica il nome dell'account batch che contiene l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c8abb-112">Specifies the name of the Batch account that contains the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8abb-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c8abb-113">-ApplicationId</span></span>
<span data-ttu-id="c8abb-114">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c8abb-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8abb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8abb-115">-DefaultProfile</span></span>
<span data-ttu-id="c8abb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8abb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8abb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8abb-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8abb-118">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="c8abb-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8abb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8abb-119">CommonParameters</span></span>
<span data-ttu-id="c8abb-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8abb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8abb-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8abb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8abb-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8abb-122">INPUTS</span></span>

### <span data-ttu-id="c8abb-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c8abb-123">None</span></span>
<span data-ttu-id="c8abb-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c8abb-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8abb-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8abb-125">OUTPUTS</span></span>

### <span data-ttu-id="c8abb-126">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="c8abb-126">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="c8abb-127">Note</span><span class="sxs-lookup"><span data-stu-id="c8abb-127">NOTES</span></span>

## <span data-ttu-id="c8abb-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8abb-128">RELATED LINKS</span></span>

[<span data-ttu-id="c8abb-129">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c8abb-129">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c8abb-130">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c8abb-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="c8abb-131">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c8abb-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c8abb-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c8abb-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="c8abb-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c8abb-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c8abb-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c8abb-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


