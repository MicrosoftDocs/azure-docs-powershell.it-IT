---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d99487ed775efe5ea36c834f28ddb3c8c301182d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674757"
---
# <span data-ttu-id="5a118-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="5a118-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="5a118-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a118-102">SYNOPSIS</span></span>
<span data-ttu-id="5a118-103">Modifica il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="5a118-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5a118-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a118-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a118-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a118-105">DESCRIPTION</span></span>
<span data-ttu-id="5a118-106">Il cmdlet **set-AzDataLakeStoreTrustedIdProvider** modifica il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="5a118-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5a118-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a118-107">EXAMPLES</span></span>

### <span data-ttu-id="5a118-108">Esempio 1: aggiornare un endpoint di tipo provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="5a118-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="5a118-109">Questo aggiornamento consente di aggiornare l'endpoint del provider per la regola del firewall "Fornisci" in account "ContosoADL" a " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="5a118-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="5a118-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a118-110">PARAMETERS</span></span>

### <span data-ttu-id="5a118-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5a118-111">-Account</span></span>
<span data-ttu-id="5a118-112">L'account di data Lake Store per aggiungere il provider di identità attendibile a</span><span class="sxs-lookup"><span data-stu-id="5a118-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="5a118-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a118-113">-DefaultProfile</span></span>
<span data-ttu-id="5a118-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5a118-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a118-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a118-115">-Name</span></span>
<span data-ttu-id="5a118-116">Nome del provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="5a118-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="5a118-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a118-117">-ProviderEndpoint</span></span>
<span data-ttu-id="5a118-118">Endpoint provider attendibile valido nel formato: https://sts.windows.net/\<provider Identity\></span><span class="sxs-lookup"><span data-stu-id="5a118-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="5a118-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a118-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a118-120">Specifica il nome del gruppo di risorse che contiene l'account per aggiornare il provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="5a118-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="5a118-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a118-121">-Confirm</span></span>
<span data-ttu-id="5a118-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a118-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a118-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a118-123">-WhatIf</span></span>
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

### <span data-ttu-id="5a118-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a118-124">CommonParameters</span></span>
<span data-ttu-id="5a118-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a118-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a118-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a118-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a118-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a118-127">INPUTS</span></span>

### <span data-ttu-id="5a118-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5a118-128">System.String</span></span>

## <span data-ttu-id="5a118-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a118-129">OUTPUTS</span></span>

### <span data-ttu-id="5a118-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="5a118-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="5a118-131">Note</span><span class="sxs-lookup"><span data-stu-id="5a118-131">NOTES</span></span>

## <span data-ttu-id="5a118-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a118-132">RELATED LINKS</span></span>
