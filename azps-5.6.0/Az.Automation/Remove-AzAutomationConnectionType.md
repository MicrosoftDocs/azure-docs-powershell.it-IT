---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 4d153a05ad245eeece671adced6aa2f8029dc9a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009965"
---
# <span data-ttu-id="eff47-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="eff47-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="eff47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eff47-102">SYNOPSIS</span></span>
<span data-ttu-id="eff47-103">Rimuove un tipo di connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="eff47-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="eff47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eff47-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eff47-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eff47-105">DESCRIPTION</span></span>
<span data-ttu-id="eff47-106">Il cmdlet **Remove-AzAutomationConnectionType** rimuove un tipo di connessione dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="eff47-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="eff47-107">Tutte le connessioni associate al tipo di connessione eliminato diventano inutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="eff47-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="eff47-108">Rimuoverli, a meno che non si crei un nuovo tipo di connessione che soddisfi i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="eff47-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="eff47-109">Il tipo ha lo stesso nome del tipo di connessione originale.</span><span class="sxs-lookup"><span data-stu-id="eff47-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="eff47-110">Il tipo ha le stesse definizioni di campo del tipo di connessione originale.</span><span class="sxs-lookup"><span data-stu-id="eff47-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="eff47-111">Può contenere altri campi.</span><span class="sxs-lookup"><span data-stu-id="eff47-111">It can have additional fields.</span></span>

## <span data-ttu-id="eff47-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eff47-112">EXAMPLES</span></span>

### <span data-ttu-id="eff47-113">Esempio 1: Rimuovere un tipo di connessione</span><span class="sxs-lookup"><span data-stu-id="eff47-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eff47-114">Questo comando rimuove un tipo di connessione denominato ContosoConnectionType nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="eff47-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="eff47-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eff47-115">PARAMETERS</span></span>

### <span data-ttu-id="eff47-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eff47-116">-AutomationAccountName</span></span>
<span data-ttu-id="eff47-117">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove un tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="eff47-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="eff47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff47-118">-DefaultProfile</span></span>
<span data-ttu-id="eff47-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eff47-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eff47-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eff47-120">-Force</span></span>
<span data-ttu-id="eff47-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="eff47-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff47-122">-Name</span><span class="sxs-lookup"><span data-stu-id="eff47-122">-Name</span></span>
<span data-ttu-id="eff47-123">Specifica il nome del tipo di connessione di automazione rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eff47-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eff47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff47-124">-ResourceGroupName</span></span>
<span data-ttu-id="eff47-125">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un tipo di connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="eff47-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eff47-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eff47-126">-Confirm</span></span>
<span data-ttu-id="eff47-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eff47-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eff47-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff47-128">-WhatIf</span></span>
<span data-ttu-id="eff47-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eff47-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eff47-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eff47-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eff47-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff47-131">CommonParameters</span></span>
<span data-ttu-id="eff47-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff47-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff47-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff47-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff47-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="eff47-134">INPUTS</span></span>

### <span data-ttu-id="eff47-135">System.String</span><span class="sxs-lookup"><span data-stu-id="eff47-135">System.String</span></span>

## <span data-ttu-id="eff47-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eff47-136">OUTPUTS</span></span>

### <span data-ttu-id="eff47-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="eff47-137">System.Void</span></span>

## <span data-ttu-id="eff47-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="eff47-138">NOTES</span></span>

## <span data-ttu-id="eff47-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eff47-139">RELATED LINKS</span></span>

[<span data-ttu-id="eff47-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="eff47-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


