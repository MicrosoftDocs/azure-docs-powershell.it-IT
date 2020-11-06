---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 1f32e700cd5d0c20e041143e43755172ecf2da86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520275"
---
# <span data-ttu-id="e71f3-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e71f3-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="e71f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e71f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e71f3-103">Ottiene le chiavi di un account batch.</span><span class="sxs-lookup"><span data-stu-id="e71f3-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e71f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e71f3-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e71f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e71f3-105">DESCRIPTION</span></span>
<span data-ttu-id="e71f3-106">Il cmdlet **Get-AzureRmBatchAccountKeys** ottiene le chiavi di un account batch di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e71f3-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="e71f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e71f3-107">EXAMPLES</span></span>

## <span data-ttu-id="e71f3-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e71f3-108">PARAMETERS</span></span>

### <span data-ttu-id="e71f3-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e71f3-109">-AccountName</span></span>
<span data-ttu-id="e71f3-110">Specifica il nome dell'account per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="e71f3-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e71f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71f3-111">-DefaultProfile</span></span>
<span data-ttu-id="e71f3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e71f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e71f3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71f3-113">-ResourceGroupName</span></span>
<span data-ttu-id="e71f3-114">Specifica il nome del gruppo di risorse che contiene l'account per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="e71f3-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e71f3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71f3-115">CommonParameters</span></span>
<span data-ttu-id="e71f3-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e71f3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71f3-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71f3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71f3-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e71f3-118">INPUTS</span></span>

### <span data-ttu-id="e71f3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e71f3-119">System.String</span></span>

## <span data-ttu-id="e71f3-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e71f3-120">OUTPUTS</span></span>

### <span data-ttu-id="e71f3-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e71f3-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e71f3-122">Note</span><span class="sxs-lookup"><span data-stu-id="e71f3-122">NOTES</span></span>

## <span data-ttu-id="e71f3-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e71f3-123">RELATED LINKS</span></span>

[<span data-ttu-id="e71f3-124">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e71f3-124">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="e71f3-125">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="e71f3-125">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


