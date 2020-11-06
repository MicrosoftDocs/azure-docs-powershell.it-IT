---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 302ad6ac14ad9fcb08053e70afb7951e72c6e027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515752"
---
# <span data-ttu-id="39e87-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="39e87-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="39e87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39e87-102">SYNOPSIS</span></span>
<span data-ttu-id="39e87-103">Aggiunge un provider di identità attendibile all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="39e87-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39e87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39e87-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39e87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39e87-105">DESCRIPTION</span></span>
<span data-ttu-id="39e87-106">Il cmdlet **Add-AzureRmDataLakeStoreTrustedIdProvider** aggiunge un provider di identità attendibile all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="39e87-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="39e87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39e87-107">EXAMPLES</span></span>

### <span data-ttu-id="39e87-108">Esempio 1: aggiungere un provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="39e87-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="39e87-109">Aggiunge il provider "provider" all'account "ContosoADL" con l'endpoint del provider " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="39e87-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="39e87-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39e87-110">PARAMETERS</span></span>

### <span data-ttu-id="39e87-111">-Account</span><span class="sxs-lookup"><span data-stu-id="39e87-111">-Account</span></span>
<span data-ttu-id="39e87-112">Nome dell'account di data Lake Store in cui aggiungere il provider di identità attendibile specificato.</span><span class="sxs-lookup"><span data-stu-id="39e87-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="39e87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e87-113">-DefaultProfile</span></span>
<span data-ttu-id="39e87-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="39e87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39e87-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="39e87-115">-Name</span></span>
<span data-ttu-id="39e87-116">Nome del provider di identità attendibile da aggiungere</span><span class="sxs-lookup"><span data-stu-id="39e87-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="39e87-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="39e87-117">-ProviderEndpoint</span></span>
<span data-ttu-id="39e87-118">Endpoint provider attendibile valido nel formato: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="39e87-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="39e87-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e87-119">-ResourceGroupName</span></span>
<span data-ttu-id="39e87-120">Nome del gruppo di risorse in cui l'account per aggiungere il provider di identità attendibile è.</span><span class="sxs-lookup"><span data-stu-id="39e87-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="39e87-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39e87-121">-Confirm</span></span>
<span data-ttu-id="39e87-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39e87-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e87-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e87-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e87-124">CommonParameters</span></span>
<span data-ttu-id="39e87-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e87-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e87-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39e87-127">INPUTS</span></span>

### <span data-ttu-id="39e87-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="39e87-128">None</span></span>
<span data-ttu-id="39e87-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="39e87-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39e87-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39e87-130">OUTPUTS</span></span>

### <span data-ttu-id="39e87-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="39e87-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="39e87-132">Il provider di identità attendibile aggiunto.</span><span class="sxs-lookup"><span data-stu-id="39e87-132">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="39e87-133">Note</span><span class="sxs-lookup"><span data-stu-id="39e87-133">NOTES</span></span>

## <span data-ttu-id="39e87-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39e87-134">RELATED LINKS</span></span>

