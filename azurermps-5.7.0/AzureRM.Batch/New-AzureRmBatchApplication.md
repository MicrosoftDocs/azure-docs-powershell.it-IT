---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 77b3d446c52e72bc31a2802768b00822982d1ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687647"
---
# <span data-ttu-id="a41e3-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a41e3-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="a41e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a41e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a41e3-103">Aggiunge un'applicazione all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="a41e3-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a41e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a41e3-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a41e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a41e3-105">DESCRIPTION</span></span>
<span data-ttu-id="a41e3-106">Il cmdlet **New-AzureRmBatchApplication** aggiunge un'applicazione all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="a41e3-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="a41e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a41e3-107">EXAMPLES</span></span>

### <span data-ttu-id="a41e3-108">Esempio 1: aggiungere un'applicazione vuota a un account batch</span><span class="sxs-lookup"><span data-stu-id="a41e3-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="a41e3-109">Questo comando crea l'applicazione Litware nell'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="a41e3-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="a41e3-110">L'applicazione inizialmente non contiene pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a41e3-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="a41e3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a41e3-111">PARAMETERS</span></span>

### <span data-ttu-id="a41e3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a41e3-112">-AccountName</span></span>
<span data-ttu-id="a41e3-113">Specifica il nome dell'account batch a cui questo cmdlet aggiunge un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a41e3-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="a41e3-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="a41e3-114">-AllowUpdates</span></span>
<span data-ttu-id="a41e3-115">Specifica se i pacchetti all'interno dell'applicazione possono essere sovrascritti usando la stessa stringa di versione.</span><span class="sxs-lookup"><span data-stu-id="a41e3-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41e3-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a41e3-116">-ApplicationId</span></span>
<span data-ttu-id="a41e3-117">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a41e3-117">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a41e3-118">-DefaultProfile</span></span>
<span data-ttu-id="a41e3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a41e3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a41e3-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a41e3-120">-DisplayName</span></span>
<span data-ttu-id="a41e3-121">Specifica il nome visualizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a41e3-121">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a41e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="a41e3-123">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="a41e3-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a41e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a41e3-124">CommonParameters</span></span>
<span data-ttu-id="a41e3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a41e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a41e3-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a41e3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a41e3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a41e3-127">INPUTS</span></span>

### <span data-ttu-id="a41e3-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a41e3-128">None</span></span>
<span data-ttu-id="a41e3-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a41e3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a41e3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a41e3-130">OUTPUTS</span></span>

### <span data-ttu-id="a41e3-131">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a41e3-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="a41e3-132">Note</span><span class="sxs-lookup"><span data-stu-id="a41e3-132">NOTES</span></span>

## <span data-ttu-id="a41e3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a41e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="a41e3-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a41e3-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="a41e3-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a41e3-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a41e3-136">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a41e3-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a41e3-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a41e3-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="a41e3-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a41e3-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a41e3-139">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a41e3-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


