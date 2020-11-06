---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: df7229668547e1c018067effe50e823354d64736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521456"
---
# <span data-ttu-id="a5117-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a5117-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="a5117-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5117-102">SYNOPSIS</span></span>
<span data-ttu-id="a5117-103">Elimina un'applicazione da un account batch.</span><span class="sxs-lookup"><span data-stu-id="a5117-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5117-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5117-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5117-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5117-105">DESCRIPTION</span></span>
<span data-ttu-id="a5117-106">Il cmdlet **Remove-AzureRmBatchApplication** Elimina un'applicazione da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5117-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="a5117-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5117-107">EXAMPLES</span></span>

### <span data-ttu-id="a5117-108">Esempio 1: eliminare un'applicazione da un account batch</span><span class="sxs-lookup"><span data-stu-id="a5117-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="a5117-109">Questo comando Elimina l'applicazione Litware dall'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="a5117-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="a5117-110">Il comando non riesce se l'applicazione contiene pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a5117-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="a5117-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5117-111">PARAMETERS</span></span>

### <span data-ttu-id="a5117-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5117-112">-AccountName</span></span>
<span data-ttu-id="a5117-113">Specifica il nome dell'account batch da cui questo cmdlet rimuove un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5117-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="a5117-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a5117-114">-ApplicationId</span></span>
<span data-ttu-id="a5117-115">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a5117-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="a5117-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5117-116">-DefaultProfile</span></span>
<span data-ttu-id="a5117-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5117-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5117-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5117-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5117-119">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="a5117-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a5117-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5117-120">CommonParameters</span></span>
<span data-ttu-id="a5117-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5117-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5117-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5117-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5117-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5117-123">INPUTS</span></span>

### <span data-ttu-id="a5117-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5117-124">None</span></span>
<span data-ttu-id="a5117-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a5117-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5117-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5117-126">OUTPUTS</span></span>

## <span data-ttu-id="a5117-127">Note</span><span class="sxs-lookup"><span data-stu-id="a5117-127">NOTES</span></span>

## <span data-ttu-id="a5117-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5117-128">RELATED LINKS</span></span>

[<span data-ttu-id="a5117-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a5117-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="a5117-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a5117-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a5117-131">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a5117-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="a5117-132">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a5117-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a5117-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a5117-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a5117-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a5117-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


