---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: a9289bc6a0db4403b96e982fd28f91578e3a0c9b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685359"
---
# <span data-ttu-id="365d8-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="365d8-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="365d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="365d8-102">SYNOPSIS</span></span>
<span data-ttu-id="365d8-103">Ottiene le chiavi di un account batch.</span><span class="sxs-lookup"><span data-stu-id="365d8-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="365d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="365d8-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="365d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="365d8-105">DESCRIPTION</span></span>
<span data-ttu-id="365d8-106">Il cmdlet **Get-AzBatchAccountKey** ottiene le chiavi di un account batch di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="365d8-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="365d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="365d8-107">EXAMPLES</span></span>

### <span data-ttu-id="365d8-108">Esempio 1: ottenere le chiavi dell'account batch e salvarlo in $Context variabile per l'uso in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="365d8-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="365d8-109">Questo comando consente di ottenere i dettagli dell'account e di archiviarli in un `$Context` oggetto per usarli in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="365d8-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="365d8-110">Esempio 2: ottenere le chiavi dell'account batch e visualizzarle</span><span class="sxs-lookup"><span data-stu-id="365d8-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="365d8-111">Questo comando consente di ottenere le chiavi dell'account e di stamparle nella console.</span><span class="sxs-lookup"><span data-stu-id="365d8-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="365d8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="365d8-112">PARAMETERS</span></span>

### <span data-ttu-id="365d8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="365d8-113">-AccountName</span></span>
<span data-ttu-id="365d8-114">Specifica il nome dell'account per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="365d8-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="365d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365d8-115">-DefaultProfile</span></span>
<span data-ttu-id="365d8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="365d8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="365d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="365d8-118">Specifica il nome del gruppo di risorse che contiene l'account per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="365d8-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="365d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365d8-119">CommonParameters</span></span>
<span data-ttu-id="365d8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365d8-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365d8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365d8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="365d8-122">INPUTS</span></span>

### <span data-ttu-id="365d8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="365d8-123">System.String</span></span>

## <span data-ttu-id="365d8-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="365d8-124">OUTPUTS</span></span>

### <span data-ttu-id="365d8-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="365d8-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="365d8-126">Note</span><span class="sxs-lookup"><span data-stu-id="365d8-126">NOTES</span></span>

## <span data-ttu-id="365d8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="365d8-127">RELATED LINKS</span></span>

[<span data-ttu-id="365d8-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="365d8-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="365d8-129">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="365d8-129">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

