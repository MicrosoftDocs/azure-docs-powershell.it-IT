---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022894"
---
# <span data-ttu-id="03410-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="03410-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="03410-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03410-102">SYNOPSIS</span></span>
<span data-ttu-id="03410-103">Rimuove una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="03410-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="03410-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03410-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03410-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03410-105">DESCRIPTION</span></span>
<span data-ttu-id="03410-106">Il cmdlet **Remove-AzAutomationConnection** rimuove una connessione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="03410-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="03410-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03410-107">EXAMPLES</span></span>

### <span data-ttu-id="03410-108">Esempio 1: rimuovere una connessione</span><span class="sxs-lookup"><span data-stu-id="03410-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="03410-109">Questo comando rimuove un certificato denominato ContosoConnection nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="03410-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="03410-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03410-110">PARAMETERS</span></span>

### <span data-ttu-id="03410-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03410-111">-AutomationAccountName</span></span>
<span data-ttu-id="03410-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="03410-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="03410-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03410-113">-DefaultProfile</span></span>
<span data-ttu-id="03410-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="03410-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03410-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03410-115">-Force</span></span>
<span data-ttu-id="03410-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="03410-116">ps_force</span></span>

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

### <span data-ttu-id="03410-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="03410-117">-Name</span></span>
<span data-ttu-id="03410-118">Specifica il nome della connessione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03410-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03410-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03410-119">-ResourceGroupName</span></span>
<span data-ttu-id="03410-120">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="03410-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="03410-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03410-121">-Confirm</span></span>
<span data-ttu-id="03410-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03410-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03410-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03410-123">-WhatIf</span></span>
<span data-ttu-id="03410-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03410-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03410-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03410-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03410-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03410-126">CommonParameters</span></span>
<span data-ttu-id="03410-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03410-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03410-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03410-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03410-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03410-129">INPUTS</span></span>

### <span data-ttu-id="03410-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03410-130">System.String</span></span>

## <span data-ttu-id="03410-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03410-131">OUTPUTS</span></span>

### <span data-ttu-id="03410-132">System. void</span><span class="sxs-lookup"><span data-stu-id="03410-132">System.Void</span></span>

## <span data-ttu-id="03410-133">Note</span><span class="sxs-lookup"><span data-stu-id="03410-133">NOTES</span></span>

## <span data-ttu-id="03410-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03410-134">RELATED LINKS</span></span>

[<span data-ttu-id="03410-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="03410-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="03410-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="03410-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


