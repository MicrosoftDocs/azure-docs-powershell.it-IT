---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: 8b0bf38d68f4dbab815b6de1f056439cd5e88e3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008126"
---
# <span data-ttu-id="17c05-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="17c05-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="17c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c05-102">SYNOPSIS</span></span>
<span data-ttu-id="17c05-103">Disabilita il ridimensionamento automatico di un pool.</span><span class="sxs-lookup"><span data-stu-id="17c05-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="17c05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17c05-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17c05-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17c05-105">DESCRIPTION</span></span>
<span data-ttu-id="17c05-106">Il cmdlet **Disable-AzBatchAutoScale** disabilita il ridimensionamento automatico del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="17c05-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="17c05-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17c05-107">EXAMPLES</span></span>

### <span data-ttu-id="17c05-108">Esempio 1: Disabilitare il ridimensionamento automatico di un pool</span><span class="sxs-lookup"><span data-stu-id="17c05-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="17c05-109">Questo comando disabilita il ridimensionamento automatico per il pool denominato MyPool.</span><span class="sxs-lookup"><span data-stu-id="17c05-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="17c05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17c05-110">PARAMETERS</span></span>

### <span data-ttu-id="17c05-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="17c05-111">-BatchContext</span></span>
<span data-ttu-id="17c05-112">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="17c05-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="17c05-113">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="17c05-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="17c05-114">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="17c05-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="17c05-115">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="17c05-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="17c05-116">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="17c05-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="17c05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c05-117">-DefaultProfile</span></span>
<span data-ttu-id="17c05-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17c05-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17c05-119">-Id</span><span class="sxs-lookup"><span data-stu-id="17c05-119">-Id</span></span>
<span data-ttu-id="17c05-120">Specifica l'ID oggetto del pool.</span><span class="sxs-lookup"><span data-stu-id="17c05-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="17c05-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c05-121">CommonParameters</span></span>
<span data-ttu-id="17c05-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c05-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c05-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17c05-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c05-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="17c05-124">INPUTS</span></span>

### <span data-ttu-id="17c05-125">System.String</span><span class="sxs-lookup"><span data-stu-id="17c05-125">System.String</span></span>

### <span data-ttu-id="17c05-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="17c05-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="17c05-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17c05-127">OUTPUTS</span></span>

### <span data-ttu-id="17c05-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="17c05-128">System.Void</span></span>

## <span data-ttu-id="17c05-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="17c05-129">NOTES</span></span>

## <span data-ttu-id="17c05-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17c05-130">RELATED LINKS</span></span>

[<span data-ttu-id="17c05-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="17c05-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="17c05-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="17c05-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="17c05-133">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="17c05-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


