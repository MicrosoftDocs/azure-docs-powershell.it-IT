---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199543"
---
# <span data-ttu-id="dec17-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dec17-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="dec17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dec17-102">SYNOPSIS</span></span>
<span data-ttu-id="dec17-103">Ottiene le chiavi di un account batch.</span><span class="sxs-lookup"><span data-stu-id="dec17-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="dec17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dec17-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dec17-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dec17-105">DESCRIPTION</span></span>
<span data-ttu-id="dec17-106">Il cmdlet **Get-AzBatchAccountKey** ottiene le chiavi di un account batch di Azure nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="dec17-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="dec17-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dec17-107">EXAMPLES</span></span>

### <span data-ttu-id="dec17-108">Esempio 1: Ottenere le chiavi dell'account batch e salvarle in una $Context variabile da usare in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="dec17-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="dec17-109">Questo comando recupera i dettagli dell'account e lo archivia in un `$Context` oggetto per usarlo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="dec17-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="dec17-110">Esempio 2: Ottenere le chiavi dell'account batch e visualizzarle</span><span class="sxs-lookup"><span data-stu-id="dec17-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="dec17-111">Questo comando recupera i tasti account e li stampa sulla console.</span><span class="sxs-lookup"><span data-stu-id="dec17-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="dec17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dec17-112">PARAMETERS</span></span>

### <span data-ttu-id="dec17-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dec17-113">-AccountName</span></span>
<span data-ttu-id="dec17-114">Specifica il nome dell'account per cui il cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="dec17-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="dec17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec17-115">-DefaultProfile</span></span>
<span data-ttu-id="dec17-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dec17-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec17-117">-ResourceGroupName</span></span>
<span data-ttu-id="dec17-118">Specifica il nome del gruppo di risorse che contiene l'account per cui il cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="dec17-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="dec17-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec17-119">CommonParameters</span></span>
<span data-ttu-id="dec17-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dec17-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec17-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dec17-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec17-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="dec17-122">INPUTS</span></span>

### <span data-ttu-id="dec17-123">System.String</span><span class="sxs-lookup"><span data-stu-id="dec17-123">System.String</span></span>

## <span data-ttu-id="dec17-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dec17-124">OUTPUTS</span></span>

### <span data-ttu-id="dec17-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dec17-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dec17-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="dec17-126">NOTES</span></span>

## <span data-ttu-id="dec17-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dec17-127">RELATED LINKS</span></span>

[<span data-ttu-id="dec17-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dec17-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="dec17-129">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="dec17-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
