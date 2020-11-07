---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 48080fde4c7187bcbcf601cb136373cc16ef7503
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865616"
---
# <span data-ttu-id="30a97-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="30a97-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="30a97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30a97-102">SYNOPSIS</span></span>
<span data-ttu-id="30a97-103">Ottiene un account batch nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="30a97-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="30a97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30a97-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30a97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30a97-105">DESCRIPTION</span></span>
<span data-ttu-id="30a97-106">Il cmdlet **Get-AzBatchAccount** ottiene un account batch di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="30a97-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="30a97-107">Puoi usare il parametro *AccountName* per ottenere un singolo account oppure puoi usare il parametro *ResourceGroupName* per ottenere gli account in tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30a97-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="30a97-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30a97-108">EXAMPLES</span></span>

### <span data-ttu-id="30a97-109">Esempio 1: ottenere un account batch per nome</span><span class="sxs-lookup"><span data-stu-id="30a97-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="30a97-110">Questo comando ottiene l'account batch denominato pfuller.</span><span class="sxs-lookup"><span data-stu-id="30a97-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="30a97-111">Esempio 2: ottenere gli account batch associati a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="30a97-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="30a97-112">Questo comando consente di ottenere gli account batch associati al gruppo di risorse CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="30a97-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="30a97-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30a97-113">PARAMETERS</span></span>

### <span data-ttu-id="30a97-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="30a97-114">-AccountName</span></span>
<span data-ttu-id="30a97-115">Specifica il nome di un account.</span><span class="sxs-lookup"><span data-stu-id="30a97-115">Specifies the name of an account.</span></span>
<span data-ttu-id="30a97-116">Se specifichi un nome account, questo cmdlet restituisce solo l'account.</span><span class="sxs-lookup"><span data-stu-id="30a97-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a97-117">-DefaultProfile</span></span>
<span data-ttu-id="30a97-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30a97-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30a97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a97-119">-ResourceGroupName</span></span>
<span data-ttu-id="30a97-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30a97-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="30a97-121">Se si specifica un gruppo di risorse, questo cmdlet ottiene gli account nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="30a97-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a97-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="30a97-122">-Tag</span></span>
<span data-ttu-id="30a97-123">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="30a97-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30a97-124">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"} questo cmdlet ottiene gli account che contengono i tag specificati da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="30a97-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a97-125">CommonParameters</span></span>
<span data-ttu-id="30a97-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a97-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30a97-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a97-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30a97-128">INPUTS</span></span>

### <span data-ttu-id="30a97-129">System. String</span><span class="sxs-lookup"><span data-stu-id="30a97-129">System.String</span></span>

### <span data-ttu-id="30a97-130">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="30a97-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30a97-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30a97-131">OUTPUTS</span></span>

### <span data-ttu-id="30a97-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="30a97-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="30a97-133">Note</span><span class="sxs-lookup"><span data-stu-id="30a97-133">NOTES</span></span>

## <span data-ttu-id="30a97-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30a97-134">RELATED LINKS</span></span>

[<span data-ttu-id="30a97-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="30a97-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="30a97-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="30a97-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="30a97-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="30a97-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="30a97-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="30a97-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
