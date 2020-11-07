---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: e996e02c9609e259c0833cfe179f295206684351
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685326"
---
# <span data-ttu-id="6c9ae-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6c9ae-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="6c9ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9ae-103">Crea un account batch.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-103">Creates a Batch account.</span></span>

## <span data-ttu-id="6c9ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c9ae-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c9ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="6c9ae-106">Il cmdlet **New-AzBatchAccount** crea un account batch di Azure per il gruppo di risorse e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="6c9ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="6c9ae-108">Esempio 1: creare un account batch</span><span class="sxs-lookup"><span data-stu-id="6c9ae-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="6c9ae-109">Questo comando crea un account batch denominato pfuller con il gruppo di risorse ResourceGroup03 nella posizione ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="6c9ae-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c9ae-110">PARAMETERS</span></span>

### <span data-ttu-id="6c9ae-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c9ae-111">-AccountName</span></span>
<span data-ttu-id="6c9ae-112">Specifica il nome dell'account batch creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="6c9ae-113">I nomi di account batch devono essere lunghi da 3 a 24 caratteri e contengono solo numeri e lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="6c9ae-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6c9ae-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="6c9ae-115">Specifica l'ID risorsa dell'account di archiviazione da usare per l'archiviazione automatica.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9ae-116">-DefaultProfile</span></span>
<span data-ttu-id="6c9ae-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c9ae-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6c9ae-118">-KeyVaultId</span></span>
<span data-ttu-id="6c9ae-119">ID risorsa dell'archivio di chiavi di Azure associato all'account batch.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="6c9ae-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="6c9ae-120">-KeyVaultUrl</span></span>
<span data-ttu-id="6c9ae-121">URL dell'archivio di chiavi di Azure associato all'account batch.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-121">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="6c9ae-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6c9ae-122">-Location</span></span>
<span data-ttu-id="6c9ae-123">Specifica l'area geografica in cui questo cmdlet crea l'account.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="6c9ae-124">Per altre informazioni, Vedi [aree di Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="6c9ae-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9ae-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="6c9ae-125">-PoolAllocationMode</span></span>
<span data-ttu-id="6c9ae-126">Modalità di assegnazione per la creazione di pool nell'account batch.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c9ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c9ae-128">Specifica il nome del gruppo di risorse in cui questo cmdlet crea l'account.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9ae-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c9ae-129">-Tag</span></span>
<span data-ttu-id="6c9ae-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6c9ae-131">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6c9ae-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9ae-132">CommonParameters</span></span>
<span data-ttu-id="6c9ae-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9ae-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9ae-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9ae-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c9ae-135">INPUTS</span></span>

### <span data-ttu-id="6c9ae-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9ae-136">System.String</span></span>

### <span data-ttu-id="6c9ae-137">System. Nullable ' 1 [[Microsoft.Azure.Management.Batch. Models. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6c9ae-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6c9ae-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c9ae-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c9ae-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c9ae-139">OUTPUTS</span></span>

### <span data-ttu-id="6c9ae-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6c9ae-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6c9ae-141">Note</span><span class="sxs-lookup"><span data-stu-id="6c9ae-141">NOTES</span></span>

## <span data-ttu-id="6c9ae-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c9ae-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c9ae-143">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6c9ae-143">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="6c9ae-144">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6c9ae-144">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="6c9ae-145">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="6c9ae-145">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="6c9ae-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="6c9ae-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
