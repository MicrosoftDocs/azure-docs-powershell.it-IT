---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: c4a8eb0bc75660c13ce8f8492b72cce8a77280e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514559"
---
# <span data-ttu-id="51c9e-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="51c9e-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="51c9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="51c9e-103">Crea un account batch.</span><span class="sxs-lookup"><span data-stu-id="51c9e-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51c9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51c9e-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51c9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51c9e-105">DESCRIPTION</span></span>
<span data-ttu-id="51c9e-106">Il cmdlet **New-AzureRmBatchAccount** crea un account batch di Azure per il gruppo di risorse e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="51c9e-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="51c9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51c9e-107">EXAMPLES</span></span>

### <span data-ttu-id="51c9e-108">Esempio 1: creare un account batch</span><span class="sxs-lookup"><span data-stu-id="51c9e-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="51c9e-109">Questo comando crea un account batch denominato pfuller con il gruppo di risorse ResourceGroup03 nella posizione ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="51c9e-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="51c9e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51c9e-110">PARAMETERS</span></span>

### <span data-ttu-id="51c9e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51c9e-111">-AccountName</span></span>
<span data-ttu-id="51c9e-112">Specifica il nome dell'account batch creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51c9e-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="51c9e-113">I nomi di account batch devono essere lunghi da 3 a 24 caratteri e contengono solo numeri e lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="51c9e-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="51c9e-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="51c9e-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="51c9e-115">Specifica l'ID risorsa dell'account di archiviazione da usare per l'archiviazione automatica.</span><span class="sxs-lookup"><span data-stu-id="51c9e-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c9e-116">-DefaultProfile</span></span>
<span data-ttu-id="51c9e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51c9e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51c9e-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="51c9e-118">-KeyVaultId</span></span>
<span data-ttu-id="51c9e-119">ID risorsa dell'archivio di chiavi di Azure associato all'account batch.</span><span class="sxs-lookup"><span data-stu-id="51c9e-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="51c9e-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="51c9e-120">-KeyVaultUrl</span></span>
<span data-ttu-id="51c9e-121">URL dell'archivio di chiavi di Azure associato all'account batch.</span><span class="sxs-lookup"><span data-stu-id="51c9e-121">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="51c9e-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="51c9e-122">-Location</span></span>
<span data-ttu-id="51c9e-123">Specifica l'area geografica in cui questo cmdlet crea l'account.</span><span class="sxs-lookup"><span data-stu-id="51c9e-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="51c9e-124">Per altre informazioni, Vedi [aree di Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="51c9e-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c9e-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="51c9e-125">-PoolAllocationMode</span></span>
<span data-ttu-id="51c9e-126">Modalità di assegnazione per la creazione di pool nell'account batch.</span><span class="sxs-lookup"><span data-stu-id="51c9e-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: PoolAllocationMode
Parameter Sets: (All)
Aliases: 
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c9e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c9e-127">-ResourceGroupName</span></span>
<span data-ttu-id="51c9e-128">Specifica il nome del gruppo di risorse in cui questo cmdlet crea l'account.</span><span class="sxs-lookup"><span data-stu-id="51c9e-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c9e-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="51c9e-129">-Tag</span></span>
<span data-ttu-id="51c9e-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="51c9e-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51c9e-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="51c9e-131">For example:</span></span>

<span data-ttu-id="51c9e-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="51c9e-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c9e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c9e-133">CommonParameters</span></span>
<span data-ttu-id="51c9e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c9e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c9e-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c9e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c9e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51c9e-136">INPUTS</span></span>

### <span data-ttu-id="51c9e-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="51c9e-137">None</span></span>
<span data-ttu-id="51c9e-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="51c9e-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51c9e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51c9e-139">OUTPUTS</span></span>

### <span data-ttu-id="51c9e-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="51c9e-140">BatchAccountContext</span></span>

## <span data-ttu-id="51c9e-141">Note</span><span class="sxs-lookup"><span data-stu-id="51c9e-141">NOTES</span></span>

## <span data-ttu-id="51c9e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51c9e-142">RELATED LINKS</span></span>

[<span data-ttu-id="51c9e-143">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="51c9e-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="51c9e-144">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="51c9e-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="51c9e-145">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="51c9e-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="51c9e-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="51c9e-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
