---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 31ac134dc580fc23876a2fd4f9b75e60b23748e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994389"
---
# <span data-ttu-id="75af0-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="75af0-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="75af0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75af0-102">SYNOPSIS</span></span>
<span data-ttu-id="75af0-103">Aggiunge un provider di identità attendibile all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="75af0-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="75af0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75af0-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75af0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75af0-105">DESCRIPTION</span></span>
<span data-ttu-id="75af0-106">Il cmdlet **Add-AzDataLakeStoreTrustedIdProvider** aggiunge un provider di identità attendibile all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="75af0-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="75af0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75af0-107">EXAMPLES</span></span>

### <span data-ttu-id="75af0-108">Esempio 1: Aggiungere un provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="75af0-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="75af0-109">Aggiunge il provider "MyProvider" all'account "ContosoADL" con l'endpoint del provider " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 " "</span><span class="sxs-lookup"><span data-stu-id="75af0-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="75af0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75af0-110">PARAMETERS</span></span>

### <span data-ttu-id="75af0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="75af0-111">-Account</span></span>
<span data-ttu-id="75af0-112">Nome dell'account Data Lake Store a cui aggiungere il provider di identità attendibile specificato.</span><span class="sxs-lookup"><span data-stu-id="75af0-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75af0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75af0-113">-DefaultProfile</span></span>
<span data-ttu-id="75af0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="75af0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75af0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="75af0-115">-Name</span></span>
<span data-ttu-id="75af0-116">Nome del provider di identità attendibile da aggiungere</span><span class="sxs-lookup"><span data-stu-id="75af0-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="75af0-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="75af0-117">-ProviderEndpoint</span></span>
<span data-ttu-id="75af0-118">Endpoint provider attendibile valido nel formato: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="75af0-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="75af0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75af0-119">-ResourceGroupName</span></span>
<span data-ttu-id="75af0-120">Nome del gruppo di risorse in cui si trova l'account in cui aggiungere il provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="75af0-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="75af0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75af0-121">-Confirm</span></span>
<span data-ttu-id="75af0-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75af0-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75af0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75af0-123">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75af0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75af0-124">CommonParameters</span></span>
<span data-ttu-id="75af0-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75af0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75af0-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75af0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75af0-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="75af0-127">INPUTS</span></span>

### <span data-ttu-id="75af0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="75af0-128">System.String</span></span>

## <span data-ttu-id="75af0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75af0-129">OUTPUTS</span></span>

### <span data-ttu-id="75af0-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="75af0-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="75af0-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="75af0-131">NOTES</span></span>

## <span data-ttu-id="75af0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75af0-132">RELATED LINKS</span></span>
