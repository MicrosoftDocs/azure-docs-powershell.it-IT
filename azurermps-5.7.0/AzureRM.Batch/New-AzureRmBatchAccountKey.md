---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 067f3be3aa668ba5402881b697d7def09cb88658
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520711"
---
# <span data-ttu-id="3cd1d-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3cd1d-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="3cd1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3cd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd1d-103">Rigenera una chiave di un account batch.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cd1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cd1d-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cd1d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cd1d-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd1d-106">Il cmdlet **New-AzureRmBatchAccountKey** rigenera la chiave primaria o secondaria di un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="3cd1d-107">Il cmdlet restituisce un oggetto **BatchAccountContext** con le proprietà Current **PrimaryAccountKey** e **SecondaryAccountKey** .</span><span class="sxs-lookup"><span data-stu-id="3cd1d-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="3cd1d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cd1d-108">EXAMPLES</span></span>

### <span data-ttu-id="3cd1d-109">Esempio 1: rigenerare la chiave dell'account principale in un account batch</span><span class="sxs-lookup"><span data-stu-id="3cd1d-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="3cd1d-110">Questo comando rigenera la chiave dell'account principale nell'account batch denominato pfuller.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="3cd1d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3cd1d-111">PARAMETERS</span></span>

### <span data-ttu-id="3cd1d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cd1d-112">-AccountName</span></span>
<span data-ttu-id="3cd1d-113">Specifica il nome dell'account batch per il quale questo cmdlet rigenera una chiave.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="3cd1d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd1d-114">-DefaultProfile</span></span>
<span data-ttu-id="3cd1d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cd1d-116">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="3cd1d-116">-KeyType</span></span>
<span data-ttu-id="3cd1d-117">Specifica il tipo di chiave che questo cmdlet rigenera.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="3cd1d-118">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3cd1d-118">Valid values are:</span></span> 

- <span data-ttu-id="3cd1d-119">Principale</span><span class="sxs-lookup"><span data-stu-id="3cd1d-119">Primary</span></span>
- <span data-ttu-id="3cd1d-120">Secondario</span><span class="sxs-lookup"><span data-stu-id="3cd1d-120">Secondary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cd1d-122">Specifica il gruppo di risorse dell'account per cui questo cmdlet rigenera una chiave.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="3cd1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd1d-123">CommonParameters</span></span>
<span data-ttu-id="3cd1d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd1d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd1d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd1d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3cd1d-126">INPUTS</span></span>

### <span data-ttu-id="3cd1d-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3cd1d-127">None</span></span>
<span data-ttu-id="3cd1d-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3cd1d-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3cd1d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cd1d-129">OUTPUTS</span></span>

### <span data-ttu-id="3cd1d-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3cd1d-130">BatchAccountContext</span></span>

## <span data-ttu-id="3cd1d-131">Note</span><span class="sxs-lookup"><span data-stu-id="3cd1d-131">NOTES</span></span>

## <span data-ttu-id="3cd1d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cd1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="3cd1d-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3cd1d-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3cd1d-134">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="3cd1d-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


