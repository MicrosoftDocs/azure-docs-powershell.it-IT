---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f71fefdce069f1786125f8c65ba94d66fb67fa56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510644"
---
# <span data-ttu-id="4e32b-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4e32b-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4e32b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e32b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e32b-103">Aggiunge un provider di identità attendibile all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="4e32b-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e32b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e32b-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e32b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e32b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e32b-106">Il cmdlet **Add-AzureRmDataLakeStoreTrustedIdProvider** aggiunge un provider di identità attendibile all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="4e32b-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="4e32b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e32b-107">EXAMPLES</span></span>

### <span data-ttu-id="4e32b-108">Esempio 1: aggiungere un provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="4e32b-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="4e32b-109">Aggiunge il provider "provider" all'account "ContosoADL" con l'endpoint del provider " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="4e32b-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="4e32b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e32b-110">PARAMETERS</span></span>

### <span data-ttu-id="4e32b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4e32b-111">-Account</span></span>
<span data-ttu-id="4e32b-112">Nome dell'account di data Lake Store in cui aggiungere il provider di identità attendibile specificato.</span><span class="sxs-lookup"><span data-stu-id="4e32b-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="4e32b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e32b-113">-Name</span></span>
<span data-ttu-id="4e32b-114">Nome del provider di identità attendibile da aggiungere</span><span class="sxs-lookup"><span data-stu-id="4e32b-114">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="4e32b-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e32b-115">-ProviderEndpoint</span></span>
<span data-ttu-id="4e32b-116">Endpoint provider attendibile valido nel formato: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="4e32b-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="4e32b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e32b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e32b-118">Nome del gruppo di risorse in cui l'account per aggiungere il provider di identità attendibile è.</span><span class="sxs-lookup"><span data-stu-id="4e32b-118">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="4e32b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e32b-119">-Confirm</span></span>
<span data-ttu-id="4e32b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e32b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e32b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e32b-121">-WhatIf</span></span>
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

### <span data-ttu-id="4e32b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e32b-122">-DefaultProfile</span></span>
<span data-ttu-id="4e32b-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e32b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e32b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e32b-124">CommonParameters</span></span>
<span data-ttu-id="4e32b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e32b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e32b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e32b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e32b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e32b-127">INPUTS</span></span>

## <span data-ttu-id="4e32b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e32b-128">OUTPUTS</span></span>

### <span data-ttu-id="4e32b-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4e32b-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="4e32b-130">Il provider di identità attendibile aggiunto.</span><span class="sxs-lookup"><span data-stu-id="4e32b-130">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="4e32b-131">Note</span><span class="sxs-lookup"><span data-stu-id="4e32b-131">NOTES</span></span>

## <span data-ttu-id="4e32b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e32b-132">RELATED LINKS</span></span>

