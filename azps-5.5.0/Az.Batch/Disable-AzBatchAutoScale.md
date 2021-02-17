---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205411"
---
# <span data-ttu-id="766ca-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="766ca-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="766ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766ca-102">SYNOPSIS</span></span>
<span data-ttu-id="766ca-103">Disabilita il ridimensionamento automatico di un pool.</span><span class="sxs-lookup"><span data-stu-id="766ca-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="766ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="766ca-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="766ca-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="766ca-105">DESCRIPTION</span></span>
<span data-ttu-id="766ca-106">Il cmdlet **Disable-AzBatchAutoScale** disabilita il ridimensionamento automatico del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="766ca-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="766ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="766ca-107">EXAMPLES</span></span>

### <span data-ttu-id="766ca-108">Esempio 1: Disabilitare il ridimensionamento automatico di un pool</span><span class="sxs-lookup"><span data-stu-id="766ca-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="766ca-109">Questo comando disabilita il ridimensionamento automatico per il pool denominato MyPool.</span><span class="sxs-lookup"><span data-stu-id="766ca-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="766ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="766ca-110">PARAMETERS</span></span>

### <span data-ttu-id="766ca-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="766ca-111">-BatchContext</span></span>
<span data-ttu-id="766ca-112">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="766ca-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="766ca-113">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="766ca-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="766ca-114">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="766ca-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="766ca-115">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="766ca-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="766ca-116">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="766ca-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="766ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766ca-117">-DefaultProfile</span></span>
<span data-ttu-id="766ca-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="766ca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="766ca-119">-Id</span><span class="sxs-lookup"><span data-stu-id="766ca-119">-Id</span></span>
<span data-ttu-id="766ca-120">Specifica l'ID oggetto del pool.</span><span class="sxs-lookup"><span data-stu-id="766ca-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="766ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766ca-121">CommonParameters</span></span>
<span data-ttu-id="766ca-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766ca-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="766ca-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766ca-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="766ca-124">INPUTS</span></span>

### <span data-ttu-id="766ca-125">System.String</span><span class="sxs-lookup"><span data-stu-id="766ca-125">System.String</span></span>

### <span data-ttu-id="766ca-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="766ca-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="766ca-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="766ca-127">OUTPUTS</span></span>

### <span data-ttu-id="766ca-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="766ca-128">System.Void</span></span>

## <span data-ttu-id="766ca-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="766ca-129">NOTES</span></span>

## <span data-ttu-id="766ca-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="766ca-130">RELATED LINKS</span></span>

[<span data-ttu-id="766ca-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="766ca-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="766ca-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="766ca-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="766ca-133">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="766ca-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


