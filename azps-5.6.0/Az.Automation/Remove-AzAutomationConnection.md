---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 0534f05bcc59a109851188c8b585badfc90d61c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009966"
---
# <span data-ttu-id="f0189-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f0189-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="f0189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0189-102">SYNOPSIS</span></span>
<span data-ttu-id="f0189-103">Rimuove una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="f0189-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="f0189-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0189-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0189-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0189-105">DESCRIPTION</span></span>
<span data-ttu-id="f0189-106">Il cmdlet **Remove-AzAutomationConnection** rimuove una connessione dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0189-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="f0189-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0189-107">EXAMPLES</span></span>

### <span data-ttu-id="f0189-108">Esempio 1: Rimuovere una connessione</span><span class="sxs-lookup"><span data-stu-id="f0189-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f0189-109">Questo comando rimuove un certificato denominato ContosoConnection nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f0189-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f0189-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0189-110">PARAMETERS</span></span>

### <span data-ttu-id="f0189-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0189-111">-AutomationAccountName</span></span>
<span data-ttu-id="f0189-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="f0189-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="f0189-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0189-113">-DefaultProfile</span></span>
<span data-ttu-id="f0189-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0189-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0189-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0189-115">-Force</span></span>
<span data-ttu-id="f0189-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="f0189-116">ps_force</span></span>

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

### <span data-ttu-id="f0189-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f0189-117">-Name</span></span>
<span data-ttu-id="f0189-118">Specifica il nome della connessione rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0189-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0189-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0189-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0189-120">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="f0189-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="f0189-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0189-121">-Confirm</span></span>
<span data-ttu-id="f0189-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0189-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0189-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0189-123">-WhatIf</span></span>
<span data-ttu-id="f0189-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0189-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0189-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0189-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0189-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0189-126">CommonParameters</span></span>
<span data-ttu-id="f0189-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0189-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0189-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0189-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0189-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0189-129">INPUTS</span></span>

### <span data-ttu-id="f0189-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f0189-130">System.String</span></span>

## <span data-ttu-id="f0189-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0189-131">OUTPUTS</span></span>

### <span data-ttu-id="f0189-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="f0189-132">System.Void</span></span>

## <span data-ttu-id="f0189-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0189-133">NOTES</span></span>

## <span data-ttu-id="f0189-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0189-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0189-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f0189-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="f0189-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f0189-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


