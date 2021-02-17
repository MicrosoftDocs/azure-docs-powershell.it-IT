---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205522"
---
# <span data-ttu-id="05786-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="05786-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="05786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05786-102">SYNOPSIS</span></span>
<span data-ttu-id="05786-103">Rimuove una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="05786-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="05786-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05786-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05786-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05786-105">DESCRIPTION</span></span>
<span data-ttu-id="05786-106">Il cmdlet **Remove-AzAutomationConnection** rimuove una connessione dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="05786-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="05786-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05786-107">EXAMPLES</span></span>

### <span data-ttu-id="05786-108">Esempio 1: Rimuovere una connessione</span><span class="sxs-lookup"><span data-stu-id="05786-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05786-109">Questo comando rimuove un certificato denominato ContosoConnection nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="05786-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="05786-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05786-110">PARAMETERS</span></span>

### <span data-ttu-id="05786-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05786-111">-AutomationAccountName</span></span>
<span data-ttu-id="05786-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="05786-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="05786-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05786-113">-DefaultProfile</span></span>
<span data-ttu-id="05786-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="05786-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05786-115">-Force</span><span class="sxs-lookup"><span data-stu-id="05786-115">-Force</span></span>
<span data-ttu-id="05786-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="05786-116">ps_force</span></span>

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

### <span data-ttu-id="05786-117">-Name</span><span class="sxs-lookup"><span data-stu-id="05786-117">-Name</span></span>
<span data-ttu-id="05786-118">Specifica il nome della connessione rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05786-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="05786-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05786-119">-ResourceGroupName</span></span>
<span data-ttu-id="05786-120">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="05786-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="05786-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05786-121">-Confirm</span></span>
<span data-ttu-id="05786-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05786-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05786-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05786-123">-WhatIf</span></span>
<span data-ttu-id="05786-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05786-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05786-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05786-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05786-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05786-126">CommonParameters</span></span>
<span data-ttu-id="05786-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05786-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05786-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05786-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05786-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="05786-129">INPUTS</span></span>

### <span data-ttu-id="05786-130">System.String</span><span class="sxs-lookup"><span data-stu-id="05786-130">System.String</span></span>

## <span data-ttu-id="05786-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05786-131">OUTPUTS</span></span>

### <span data-ttu-id="05786-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="05786-132">System.Void</span></span>

## <span data-ttu-id="05786-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="05786-133">NOTES</span></span>

## <span data-ttu-id="05786-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05786-134">RELATED LINKS</span></span>

[<span data-ttu-id="05786-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="05786-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="05786-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="05786-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


