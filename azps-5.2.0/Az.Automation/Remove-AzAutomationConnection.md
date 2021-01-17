---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373348"
---
# <span data-ttu-id="cdcd4-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cdcd4-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="cdcd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdcd4-102">SYNOPSIS</span></span>
<span data-ttu-id="cdcd4-103">Rimuove una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="cdcd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdcd4-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdcd4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdcd4-105">DESCRIPTION</span></span>
<span data-ttu-id="cdcd4-106">Il cmdlet **Remove-AzAutomationConnection** rimuove una connessione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="cdcd4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdcd4-107">EXAMPLES</span></span>

### <span data-ttu-id="cdcd4-108">Esempio 1: rimuovere una connessione</span><span class="sxs-lookup"><span data-stu-id="cdcd4-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cdcd4-109">Questo comando rimuove un certificato denominato ContosoConnection nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cdcd4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdcd4-110">PARAMETERS</span></span>

### <span data-ttu-id="cdcd4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cdcd4-111">-AutomationAccountName</span></span>
<span data-ttu-id="cdcd4-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="cdcd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdcd4-113">-DefaultProfile</span></span>
<span data-ttu-id="cdcd4-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cdcd4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdcd4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cdcd4-115">-Force</span></span>
<span data-ttu-id="cdcd4-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="cdcd4-116">ps_force</span></span>

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

### <span data-ttu-id="cdcd4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdcd4-117">-Name</span></span>
<span data-ttu-id="cdcd4-118">Specifica il nome della connessione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cdcd4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdcd4-119">-ResourceGroupName</span></span>
<span data-ttu-id="cdcd4-120">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="cdcd4-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdcd4-121">-Confirm</span></span>
<span data-ttu-id="cdcd4-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdcd4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdcd4-123">-WhatIf</span></span>
<span data-ttu-id="cdcd4-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdcd4-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdcd4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdcd4-126">CommonParameters</span></span>
<span data-ttu-id="cdcd4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdcd4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdcd4-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdcd4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdcd4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdcd4-129">INPUTS</span></span>

### <span data-ttu-id="cdcd4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cdcd4-130">System.String</span></span>

## <span data-ttu-id="cdcd4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdcd4-131">OUTPUTS</span></span>

### <span data-ttu-id="cdcd4-132">System. void</span><span class="sxs-lookup"><span data-stu-id="cdcd4-132">System.Void</span></span>

## <span data-ttu-id="cdcd4-133">Note</span><span class="sxs-lookup"><span data-stu-id="cdcd4-133">NOTES</span></span>

## <span data-ttu-id="cdcd4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdcd4-134">RELATED LINKS</span></span>

[<span data-ttu-id="cdcd4-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cdcd4-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="cdcd4-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cdcd4-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


