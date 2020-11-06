---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508391"
---
# <span data-ttu-id="a90a8-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a90a8-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="a90a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a90a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a90a8-103">Ottiene le chiavi di un account batch.</span><span class="sxs-lookup"><span data-stu-id="a90a8-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a90a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a90a8-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a90a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a90a8-105">DESCRIPTION</span></span>
<span data-ttu-id="a90a8-106">Il cmdlet **Get-AzureRmBatchAccountKeys** ottiene le chiavi di un account batch di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a90a8-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="a90a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a90a8-107">EXAMPLES</span></span>

## <span data-ttu-id="a90a8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a90a8-108">PARAMETERS</span></span>

### <span data-ttu-id="a90a8-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a90a8-109">-AccountName</span></span>
<span data-ttu-id="a90a8-110">Specifica il nome dell'account per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="a90a8-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a90a8-111">-DefaultProfile</span></span>
<span data-ttu-id="a90a8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a90a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a90a8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90a8-113">-ResourceGroupName</span></span>
<span data-ttu-id="a90a8-114">Specifica il nome del gruppo di risorse che contiene l'account per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="a90a8-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90a8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90a8-115">CommonParameters</span></span>
<span data-ttu-id="a90a8-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a90a8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90a8-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a90a8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90a8-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a90a8-118">INPUTS</span></span>

### <span data-ttu-id="a90a8-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a90a8-119">None</span></span>
<span data-ttu-id="a90a8-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a90a8-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a90a8-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a90a8-121">OUTPUTS</span></span>

### <span data-ttu-id="a90a8-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a90a8-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a90a8-123">Note</span><span class="sxs-lookup"><span data-stu-id="a90a8-123">NOTES</span></span>

## <span data-ttu-id="a90a8-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a90a8-124">RELATED LINKS</span></span>

[<span data-ttu-id="a90a8-125">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a90a8-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="a90a8-126">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a90a8-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


