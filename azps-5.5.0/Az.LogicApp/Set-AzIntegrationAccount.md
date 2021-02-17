---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192286"
---
# <span data-ttu-id="15314-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15314-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="15314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15314-102">SYNOPSIS</span></span>
<span data-ttu-id="15314-103">Modifica un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15314-103">Modifies an integration account.</span></span>

## <span data-ttu-id="15314-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15314-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15314-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15314-105">DESCRIPTION</span></span>
<span data-ttu-id="15314-106">Il cmdlet **Set-AzIntegrationAccount** modifica un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15314-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="15314-107">Questo cmdlet restituisce un oggetto che rappresenta l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15314-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="15314-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="15314-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="15314-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="15314-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="15314-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="15314-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="15314-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="15314-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="15314-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15314-112">EXAMPLES</span></span>

### <span data-ttu-id="15314-113">Esempio 1: Modificare un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="15314-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="15314-114">Questo comando modifica un account di integrazione denominato IntegrationAccount31 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="15314-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="15314-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15314-115">PARAMETERS</span></span>

### <span data-ttu-id="15314-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15314-116">-DefaultProfile</span></span>
<span data-ttu-id="15314-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="15314-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15314-118">-Force</span><span class="sxs-lookup"><span data-stu-id="15314-118">-Force</span></span>
<span data-ttu-id="15314-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="15314-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15314-120">-Location</span><span class="sxs-lookup"><span data-stu-id="15314-120">-Location</span></span>
<span data-ttu-id="15314-121">Specifica una posizione per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15314-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="15314-122">-Name</span><span class="sxs-lookup"><span data-stu-id="15314-122">-Name</span></span>
<span data-ttu-id="15314-123">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15314-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15314-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15314-124">-ResourceGroupName</span></span>
<span data-ttu-id="15314-125">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15314-125">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15314-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="15314-126">-Sku</span></span>
<span data-ttu-id="15314-127">Specifica un nome di SKU per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15314-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15314-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15314-128">-Confirm</span></span>
<span data-ttu-id="15314-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15314-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15314-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15314-130">-WhatIf</span></span>
<span data-ttu-id="15314-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15314-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15314-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15314-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15314-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15314-133">CommonParameters</span></span>
<span data-ttu-id="15314-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15314-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15314-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15314-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15314-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="15314-136">INPUTS</span></span>

### <span data-ttu-id="15314-137">System.String</span><span class="sxs-lookup"><span data-stu-id="15314-137">System.String</span></span>

## <span data-ttu-id="15314-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15314-138">OUTPUTS</span></span>

### <span data-ttu-id="15314-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15314-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="15314-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="15314-140">NOTES</span></span>

## <span data-ttu-id="15314-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15314-141">RELATED LINKS</span></span>

[<span data-ttu-id="15314-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15314-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="15314-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15314-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="15314-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15314-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


