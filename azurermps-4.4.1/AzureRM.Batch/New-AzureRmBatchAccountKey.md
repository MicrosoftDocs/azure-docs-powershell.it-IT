---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: fbfcbaa0fdf790daad05aece6190396c735f9fff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686234"
---
# <span data-ttu-id="851e1-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="851e1-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="851e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="851e1-102">SYNOPSIS</span></span>
<span data-ttu-id="851e1-103">Rigenera una chiave di un account batch.</span><span class="sxs-lookup"><span data-stu-id="851e1-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="851e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="851e1-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="851e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="851e1-105">DESCRIPTION</span></span>
<span data-ttu-id="851e1-106">Il cmdlet **New-AzureRmBatchAccountKey** rigenera la chiave primaria o secondaria di un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="851e1-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="851e1-107">Il cmdlet restituisce un oggetto **BatchAccountContext** con le proprietà Current **PrimaryAccountKey** e **SecondaryAccountKey** .</span><span class="sxs-lookup"><span data-stu-id="851e1-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="851e1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="851e1-108">EXAMPLES</span></span>

### <span data-ttu-id="851e1-109">Esempio 1: rigenerare la chiave dell'account principale in un account batch</span><span class="sxs-lookup"><span data-stu-id="851e1-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="851e1-110">Questo comando rigenera la chiave dell'account principale nell'account batch denominato pfuller.</span><span class="sxs-lookup"><span data-stu-id="851e1-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="851e1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="851e1-111">PARAMETERS</span></span>

### <span data-ttu-id="851e1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="851e1-112">-AccountName</span></span>
<span data-ttu-id="851e1-113">Specifica il nome dell'account batch per il quale questo cmdlet rigenera una chiave.</span><span class="sxs-lookup"><span data-stu-id="851e1-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="851e1-114">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="851e1-114">-KeyType</span></span>
<span data-ttu-id="851e1-115">Specifica il tipo di chiave che questo cmdlet rigenera.</span><span class="sxs-lookup"><span data-stu-id="851e1-115">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="851e1-116">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="851e1-116">Valid values are:</span></span> 

- <span data-ttu-id="851e1-117">Principale</span><span class="sxs-lookup"><span data-stu-id="851e1-117">Primary</span></span>
- <span data-ttu-id="851e1-118">Secondario</span><span class="sxs-lookup"><span data-stu-id="851e1-118">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="851e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="851e1-120">Specifica il gruppo di risorse dell'account per cui questo cmdlet rigenera una chiave.</span><span class="sxs-lookup"><span data-stu-id="851e1-120">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="851e1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851e1-121">-DefaultProfile</span></span>
<span data-ttu-id="851e1-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="851e1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="851e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851e1-123">CommonParameters</span></span>
<span data-ttu-id="851e1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851e1-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="851e1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851e1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="851e1-126">INPUTS</span></span>

## <span data-ttu-id="851e1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="851e1-127">OUTPUTS</span></span>

### <span data-ttu-id="851e1-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="851e1-128">BatchAccountContext</span></span>

## <span data-ttu-id="851e1-129">Note</span><span class="sxs-lookup"><span data-stu-id="851e1-129">NOTES</span></span>

## <span data-ttu-id="851e1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="851e1-130">RELATED LINKS</span></span>

[<span data-ttu-id="851e1-131">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="851e1-131">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="851e1-132">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="851e1-132">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


