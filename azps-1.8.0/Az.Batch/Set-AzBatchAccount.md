---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 0a19ede4a990b10244204d8f633ed747adb7d30e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685291"
---
# <span data-ttu-id="7cf3e-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7cf3e-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="7cf3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cf3e-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf3e-103">Aggiorna un account batch.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-103">Updates a Batch account.</span></span>

## <span data-ttu-id="7cf3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cf3e-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cf3e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cf3e-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf3e-106">Il cmdlet **set-AzBatchAccount** aggiorna un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="7cf3e-107">Al momento, questo cmdlet può aggiornare solo i tag.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="7cf3e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cf3e-108">EXAMPLES</span></span>

### <span data-ttu-id="7cf3e-109">Esempio 1: aggiornare i tag in un account batch</span><span class="sxs-lookup"><span data-stu-id="7cf3e-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="7cf3e-110">Questo comando Aggiorna i tag nell'account denominato pfuller.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="7cf3e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cf3e-111">PARAMETERS</span></span>

### <span data-ttu-id="7cf3e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7cf3e-112">-AccountName</span></span>
<span data-ttu-id="7cf3e-113">Specifica il nome dell'account batch che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7cf3e-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7cf3e-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="7cf3e-115">Specifica l'ID risorsa dell'account di archiviazione da usare per l'archiviazione automatica.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="7cf3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf3e-116">-DefaultProfile</span></span>
<span data-ttu-id="7cf3e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf3e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf3e-118">-ResourceGroupName</span></span>
<span data-ttu-id="7cf3e-119">Specifica il gruppo di risorse dell'account che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7cf3e-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="7cf3e-120">-Tag</span></span>
<span data-ttu-id="7cf3e-121">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7cf3e-122">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7cf3e-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf3e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf3e-123">CommonParameters</span></span>
<span data-ttu-id="7cf3e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf3e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf3e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf3e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf3e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cf3e-126">INPUTS</span></span>

### <span data-ttu-id="7cf3e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf3e-127">System.String</span></span>

### <span data-ttu-id="7cf3e-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7cf3e-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7cf3e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cf3e-129">OUTPUTS</span></span>

### <span data-ttu-id="7cf3e-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7cf3e-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7cf3e-131">Note</span><span class="sxs-lookup"><span data-stu-id="7cf3e-131">NOTES</span></span>

## <span data-ttu-id="7cf3e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cf3e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7cf3e-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7cf3e-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="7cf3e-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7cf3e-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="7cf3e-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7cf3e-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="7cf3e-136">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="7cf3e-136">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)