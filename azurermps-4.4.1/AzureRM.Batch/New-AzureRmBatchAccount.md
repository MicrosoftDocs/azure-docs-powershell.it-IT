---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686233"
---
# <span data-ttu-id="1ad6b-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="1ad6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ad6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad6b-103">Crea un account batch.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ad6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ad6b-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ad6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ad6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad6b-106">Il cmdlet **New-AzureRmBatchAccount** crea un account batch di Azure per il gruppo di risorse e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="1ad6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ad6b-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad6b-108">Esempio 1: creare un account batch</span><span class="sxs-lookup"><span data-stu-id="1ad6b-108">Example 1: Create a Batch account</span></span>
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

<span data-ttu-id="1ad6b-109">Questo comando crea un account batch denominato pfuller con il gruppo di risorse ResourceGroup03 nella posizione ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="1ad6b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ad6b-110">PARAMETERS</span></span>

### <span data-ttu-id="1ad6b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ad6b-111">-AccountName</span></span>
<span data-ttu-id="1ad6b-112">Specifica il nome dell'account batch creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="1ad6b-113">I nomi di account batch devono essere lunghi da 3 a 24 caratteri e contengono solo numeri e lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="1ad6b-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1ad6b-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="1ad6b-115">Specifica l'ID risorsa dell'account di archiviazione da usare per l'archiviazione automatica.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="1ad6b-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1ad6b-116">-Location</span></span>
<span data-ttu-id="1ad6b-117">Specifica l'area geografica in cui questo cmdlet crea l'account.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="1ad6b-118">Per altre informazioni, Vedi [aree di Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="1ad6b-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="1ad6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ad6b-120">Specifica il nome del gruppo di risorse in cui questo cmdlet crea l'account.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="1ad6b-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ad6b-121">-Tag</span></span>
<span data-ttu-id="1ad6b-122">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ad6b-123">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="1ad6b-123">For example:</span></span>

<span data-ttu-id="1ad6b-124">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1ad6b-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ad6b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-125">-DefaultProfile</span></span>
<span data-ttu-id="1ad6b-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ad6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad6b-127">CommonParameters</span></span>
<span data-ttu-id="1ad6b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad6b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad6b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad6b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ad6b-130">INPUTS</span></span>

## <span data-ttu-id="1ad6b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ad6b-131">OUTPUTS</span></span>

### <span data-ttu-id="1ad6b-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1ad6b-132">BatchAccountContext</span></span>

## <span data-ttu-id="1ad6b-133">Note</span><span class="sxs-lookup"><span data-stu-id="1ad6b-133">NOTES</span></span>

## <span data-ttu-id="1ad6b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ad6b-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ad6b-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="1ad6b-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="1ad6b-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1ad6b-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="1ad6b-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="1ad6b-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
