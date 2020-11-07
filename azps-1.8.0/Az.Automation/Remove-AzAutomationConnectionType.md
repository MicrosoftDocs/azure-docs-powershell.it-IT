---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: ab8d51b4a1b7a66e90a61fa4903d9373dd98eb9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684999"
---
# <span data-ttu-id="584e9-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="584e9-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="584e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="584e9-102">SYNOPSIS</span></span>
<span data-ttu-id="584e9-103">Rimuove un tipo di connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="584e9-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="584e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="584e9-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="584e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="584e9-105">DESCRIPTION</span></span>
<span data-ttu-id="584e9-106">Il cmdlet **Remove-AzAutomationConnectionType** rimuove un tipo di connessione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="584e9-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="584e9-107">Tutte le connessioni associate al tipo di connessione eliminate diventano inutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="584e9-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="584e9-108">Rimuoverli, a meno che non si crei un nuovo tipo di connessione che soddisfi i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="584e9-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="584e9-109">Il tipo ha lo stesso nome del tipo di connessione originale.</span><span class="sxs-lookup"><span data-stu-id="584e9-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="584e9-110">Il tipo ha le stesse definizioni di campo del tipo di connessione originale.</span><span class="sxs-lookup"><span data-stu-id="584e9-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="584e9-111">Può avere campi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="584e9-111">It can have additional fields.</span></span>

## <span data-ttu-id="584e9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="584e9-112">EXAMPLES</span></span>

### <span data-ttu-id="584e9-113">Esempio 1: rimuovere un tipo di connessione</span><span class="sxs-lookup"><span data-stu-id="584e9-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="584e9-114">Questo comando rimuove un tipo di connessione denominato ContosoConnectionType nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="584e9-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="584e9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="584e9-115">PARAMETERS</span></span>

### <span data-ttu-id="584e9-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="584e9-116">-AutomationAccountName</span></span>
<span data-ttu-id="584e9-117">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove un tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="584e9-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="584e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="584e9-118">-DefaultProfile</span></span>
<span data-ttu-id="584e9-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="584e9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="584e9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="584e9-120">-Force</span></span>
<span data-ttu-id="584e9-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="584e9-121">ps_force</span></span>

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

### <span data-ttu-id="584e9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="584e9-122">-Name</span></span>
<span data-ttu-id="584e9-123">Specifica il nome del tipo di connessione di automazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="584e9-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="584e9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="584e9-124">-ResourceGroupName</span></span>
<span data-ttu-id="584e9-125">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un tipo di connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="584e9-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="584e9-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="584e9-126">-Confirm</span></span>
<span data-ttu-id="584e9-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="584e9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="584e9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="584e9-128">-WhatIf</span></span>
<span data-ttu-id="584e9-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="584e9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="584e9-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="584e9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="584e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="584e9-131">CommonParameters</span></span>
<span data-ttu-id="584e9-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="584e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="584e9-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="584e9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="584e9-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="584e9-134">INPUTS</span></span>

### <span data-ttu-id="584e9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="584e9-135">System.String</span></span>

## <span data-ttu-id="584e9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="584e9-136">OUTPUTS</span></span>

### <span data-ttu-id="584e9-137">System. void</span><span class="sxs-lookup"><span data-stu-id="584e9-137">System.Void</span></span>

## <span data-ttu-id="584e9-138">Note</span><span class="sxs-lookup"><span data-stu-id="584e9-138">NOTES</span></span>

## <span data-ttu-id="584e9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="584e9-139">RELATED LINKS</span></span>

[<span data-ttu-id="584e9-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="584e9-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


