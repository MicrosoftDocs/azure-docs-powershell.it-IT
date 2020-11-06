---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521050"
---
# <span data-ttu-id="01f5c-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="01f5c-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="01f5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="01f5c-103">Ottiene il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="01f5c-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="01f5c-104">Se non viene specificato alcun provider, elenca tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="01f5c-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f5c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01f5c-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f5c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01f5c-106">DESCRIPTION</span></span>
<span data-ttu-id="01f5c-107">Il cmdlet **Get-AzureRmDataLakeStoreTrustedIdProvider** ottiene il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="01f5c-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="01f5c-108">Se non viene specificato alcun provider, elenca tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="01f5c-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="01f5c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01f5c-109">EXAMPLES</span></span>

### <span data-ttu-id="01f5c-110">Esempio 1: ottenere un provider di identità attendibile specifico</span><span class="sxs-lookup"><span data-stu-id="01f5c-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="01f5c-111">Restituisce il provider denominato "metodo di fornitura" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="01f5c-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="01f5c-112">Esempio 2: elenca tutti i provider in un account</span><span class="sxs-lookup"><span data-stu-id="01f5c-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="01f5c-113">Elenca tutti i provider sotto l'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="01f5c-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="01f5c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01f5c-114">PARAMETERS</span></span>

### <span data-ttu-id="01f5c-115">-Account</span><span class="sxs-lookup"><span data-stu-id="01f5c-115">-Account</span></span>
<span data-ttu-id="01f5c-116">L'account di data Lake Store per recuperare il provider di identità attendibile da</span><span class="sxs-lookup"><span data-stu-id="01f5c-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f5c-117">-DefaultProfile</span></span>
<span data-ttu-id="01f5c-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="01f5c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01f5c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="01f5c-119">-Name</span></span>
<span data-ttu-id="01f5c-120">Nome del provider di identità attendibile da recuperare</span><span class="sxs-lookup"><span data-stu-id="01f5c-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f5c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f5c-121">-ResourceGroupName</span></span>
<span data-ttu-id="01f5c-122">Nome del gruppo di risorse in cui si vuole recuperare il provider di identità attendibile specificato dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="01f5c-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f5c-123">CommonParameters</span></span>
<span data-ttu-id="01f5c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f5c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f5c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f5c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01f5c-126">INPUTS</span></span>

### <span data-ttu-id="01f5c-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="01f5c-127">None</span></span>
<span data-ttu-id="01f5c-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="01f5c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01f5c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01f5c-129">OUTPUTS</span></span>

### <span data-ttu-id="01f5c-130">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="01f5c-130">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="01f5c-131">Dettagli del provider di identità attendibile specificato.</span><span class="sxs-lookup"><span data-stu-id="01f5c-131">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="01f5c-132">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="01f5c-132">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="01f5c-133">L'elenco dei provider di identità attendibili nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="01f5c-133">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="01f5c-134">Note</span><span class="sxs-lookup"><span data-stu-id="01f5c-134">NOTES</span></span>

## <span data-ttu-id="01f5c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01f5c-135">RELATED LINKS</span></span>

