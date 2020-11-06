---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 29f9bbab5d3f7590d53bc405d80ea9e5c484fd5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516800"
---
# <span data-ttu-id="6e225-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6e225-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="6e225-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e225-102">SYNOPSIS</span></span>
<span data-ttu-id="6e225-103">Modifica il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="6e225-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e225-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e225-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e225-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e225-105">DESCRIPTION</span></span>
<span data-ttu-id="6e225-106">Il cmdlet **set-AzureRmDataLakeStoreTrustedIdProvider** modifica il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="6e225-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6e225-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e225-107">EXAMPLES</span></span>

### <span data-ttu-id="6e225-108">Esempio 1: aggiornare un endpoint di tipo provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="6e225-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="6e225-109">Questo aggiornamento consente di aggiornare il provider endpoing per la regola del firewall "Fornisci" in account "ContosoADL" a " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="6e225-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="6e225-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e225-110">PARAMETERS</span></span>

### <span data-ttu-id="6e225-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6e225-111">-Account</span></span>
<span data-ttu-id="6e225-112">L'account di data Lake Store per aggiungere il provider di identità attendibile a</span><span class="sxs-lookup"><span data-stu-id="6e225-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="6e225-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e225-113">-DefaultProfile</span></span>
<span data-ttu-id="6e225-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6e225-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e225-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e225-115">-Name</span></span>
<span data-ttu-id="6e225-116">Nome del provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="6e225-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="6e225-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e225-117">-ProviderEndpoint</span></span>
<span data-ttu-id="6e225-118">Endpoint provider attendibile valido nel formato: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="6e225-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="6e225-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e225-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e225-120">Specifica il nome del gruppo di risorse che contiene l'account per aggiornare il provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="6e225-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="6e225-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e225-121">-Confirm</span></span>
<span data-ttu-id="6e225-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e225-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e225-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e225-123">-WhatIf</span></span>
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

### <span data-ttu-id="6e225-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e225-124">CommonParameters</span></span>
<span data-ttu-id="6e225-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e225-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e225-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e225-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e225-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e225-127">INPUTS</span></span>

### <span data-ttu-id="6e225-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6e225-128">None</span></span>
<span data-ttu-id="6e225-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6e225-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e225-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e225-130">OUTPUTS</span></span>

### <span data-ttu-id="6e225-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6e225-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="6e225-132">Provider di identità attendibile aggiornato.</span><span class="sxs-lookup"><span data-stu-id="6e225-132">The updated trusted identity provider.</span></span>

## <span data-ttu-id="6e225-133">Note</span><span class="sxs-lookup"><span data-stu-id="6e225-133">NOTES</span></span>

## <span data-ttu-id="6e225-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e225-134">RELATED LINKS</span></span>

