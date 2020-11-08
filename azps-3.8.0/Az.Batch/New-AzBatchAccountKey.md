---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: e079701f0d2ccca49e1368edc9446c08b4549c11
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030679"
---
# <span data-ttu-id="ff8b8-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff8b8-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="ff8b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8b8-103">Rigenera una chiave di un account batch.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="ff8b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff8b8-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff8b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff8b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ff8b8-106">Il cmdlet **New-AzBatchAccountKey** rigenera la chiave primaria o secondaria di un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="ff8b8-107">Il cmdlet restituisce un oggetto **BatchAccountContext** con le proprietà Current **PrimaryAccountKey** e **SecondaryAccountKey** .</span><span class="sxs-lookup"><span data-stu-id="ff8b8-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="ff8b8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff8b8-108">EXAMPLES</span></span>

### <span data-ttu-id="ff8b8-109">Esempio 1: rigenerare la chiave dell'account principale in un account batch</span><span class="sxs-lookup"><span data-stu-id="ff8b8-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="ff8b8-110">Questo comando rigenera la chiave dell'account principale nell'account batch denominato pfuller.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="ff8b8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff8b8-111">PARAMETERS</span></span>

### <span data-ttu-id="ff8b8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff8b8-112">-AccountName</span></span>
<span data-ttu-id="ff8b8-113">Specifica il nome dell'account batch per il quale questo cmdlet rigenera una chiave.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ff8b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff8b8-114">-DefaultProfile</span></span>
<span data-ttu-id="ff8b8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff8b8-116">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="ff8b8-116">-KeyType</span></span>
<span data-ttu-id="ff8b8-117">Specifica il tipo di chiave che questo cmdlet rigenera.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="ff8b8-118">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ff8b8-118">Valid values are:</span></span> 
- <span data-ttu-id="ff8b8-119">Principale</span><span class="sxs-lookup"><span data-stu-id="ff8b8-119">Primary</span></span>
- <span data-ttu-id="ff8b8-120">Secondario</span><span class="sxs-lookup"><span data-stu-id="ff8b8-120">Secondary</span></span>

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

### <span data-ttu-id="ff8b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff8b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff8b8-122">Specifica il gruppo di risorse dell'account per cui questo cmdlet rigenera una chiave.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ff8b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8b8-123">CommonParameters</span></span>
<span data-ttu-id="ff8b8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff8b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8b8-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff8b8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8b8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff8b8-126">INPUTS</span></span>

### <span data-ttu-id="ff8b8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ff8b8-127">System.String</span></span>

## <span data-ttu-id="ff8b8-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff8b8-128">OUTPUTS</span></span>

### <span data-ttu-id="ff8b8-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ff8b8-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ff8b8-130">Note</span><span class="sxs-lookup"><span data-stu-id="ff8b8-130">NOTES</span></span>

## <span data-ttu-id="ff8b8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff8b8-131">RELATED LINKS</span></span>

[<span data-ttu-id="ff8b8-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff8b8-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ff8b8-133">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="ff8b8-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


