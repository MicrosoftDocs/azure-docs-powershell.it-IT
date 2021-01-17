---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330319"
---
# <span data-ttu-id="fecdc-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="fecdc-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="fecdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fecdc-102">SYNOPSIS</span></span>
<span data-ttu-id="fecdc-103">Modifica il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="fecdc-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="fecdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fecdc-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fecdc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fecdc-105">DESCRIPTION</span></span>
<span data-ttu-id="fecdc-106">Il cmdlet **set-AzDataLakeStoreTrustedIdProvider** modifica il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="fecdc-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="fecdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fecdc-107">EXAMPLES</span></span>

### <span data-ttu-id="fecdc-108">Esempio 1: aggiornare un endpoint di tipo provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="fecdc-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="fecdc-109">Questo aggiornamento consente di aggiornare l'endpoint del provider per la regola del firewall "Fornisci" in account "ContosoADL" a " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="fecdc-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="fecdc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fecdc-110">PARAMETERS</span></span>

### <span data-ttu-id="fecdc-111">-Account</span><span class="sxs-lookup"><span data-stu-id="fecdc-111">-Account</span></span>
<span data-ttu-id="fecdc-112">L'account di data Lake Store per aggiungere il provider di identità attendibile a</span><span class="sxs-lookup"><span data-stu-id="fecdc-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="fecdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecdc-113">-DefaultProfile</span></span>
<span data-ttu-id="fecdc-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fecdc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fecdc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fecdc-115">-Name</span></span>
<span data-ttu-id="fecdc-116">Nome del provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="fecdc-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="fecdc-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="fecdc-117">-ProviderEndpoint</span></span>
<span data-ttu-id="fecdc-118">Endpoint provider attendibile valido nel formato: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="fecdc-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="fecdc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fecdc-119">-ResourceGroupName</span></span>
<span data-ttu-id="fecdc-120">Specifica il nome del gruppo di risorse che contiene l'account per aggiornare il provider di identità attendibile.</span><span class="sxs-lookup"><span data-stu-id="fecdc-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="fecdc-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fecdc-121">-Confirm</span></span>
<span data-ttu-id="fecdc-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fecdc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fecdc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fecdc-123">-WhatIf</span></span>
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

### <span data-ttu-id="fecdc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecdc-124">CommonParameters</span></span>
<span data-ttu-id="fecdc-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fecdc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecdc-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fecdc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecdc-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fecdc-127">INPUTS</span></span>

### <span data-ttu-id="fecdc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fecdc-128">System.String</span></span>

## <span data-ttu-id="fecdc-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fecdc-129">OUTPUTS</span></span>

### <span data-ttu-id="fecdc-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="fecdc-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="fecdc-131">Note</span><span class="sxs-lookup"><span data-stu-id="fecdc-131">NOTES</span></span>

## <span data-ttu-id="fecdc-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fecdc-132">RELATED LINKS</span></span>
