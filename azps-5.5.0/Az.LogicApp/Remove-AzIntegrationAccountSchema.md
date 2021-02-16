---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194207"
---
# <span data-ttu-id="af591-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af591-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="af591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af591-102">SYNOPSIS</span></span>
<span data-ttu-id="af591-103">Rimuove uno schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="af591-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="af591-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af591-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af591-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="af591-105">DESCRIPTION</span></span>
<span data-ttu-id="af591-106">Il cmdlet **Remove-AzIntegrationAccountSchema rimuove** uno schema dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af591-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="af591-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="af591-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="af591-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="af591-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="af591-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="af591-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="af591-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="af591-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="af591-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="af591-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="af591-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af591-112">EXAMPLES</span></span>

### <span data-ttu-id="af591-113">Esempio 1: Rimuovere uno schema dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="af591-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="af591-114">Questo comando rimuove uno schema dell'account di integrazione denominato IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="af591-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="af591-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af591-115">PARAMETERS</span></span>

### <span data-ttu-id="af591-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af591-116">-DefaultProfile</span></span>
<span data-ttu-id="af591-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="af591-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af591-118">-Force</span><span class="sxs-lookup"><span data-stu-id="af591-118">-Force</span></span>
<span data-ttu-id="af591-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="af591-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af591-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af591-120">-Name</span></span>
<span data-ttu-id="af591-121">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="af591-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af591-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af591-122">-ResourceGroupName</span></span>
<span data-ttu-id="af591-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af591-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="af591-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="af591-124">-SchemaName</span></span>
<span data-ttu-id="af591-125">Specifica il nome di uno schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="af591-125">Specifies the name of an integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af591-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af591-126">-Confirm</span></span>
<span data-ttu-id="af591-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af591-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af591-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af591-128">-WhatIf</span></span>
<span data-ttu-id="af591-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af591-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af591-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af591-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af591-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af591-131">CommonParameters</span></span>
<span data-ttu-id="af591-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af591-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af591-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af591-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af591-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="af591-134">INPUTS</span></span>

### <span data-ttu-id="af591-135">System.String</span><span class="sxs-lookup"><span data-stu-id="af591-135">System.String</span></span>

## <span data-ttu-id="af591-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af591-136">OUTPUTS</span></span>

### <span data-ttu-id="af591-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="af591-137">System.Void</span></span>

## <span data-ttu-id="af591-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="af591-138">NOTES</span></span>

## <span data-ttu-id="af591-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af591-139">RELATED LINKS</span></span>

[<span data-ttu-id="af591-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af591-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="af591-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af591-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="af591-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af591-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


