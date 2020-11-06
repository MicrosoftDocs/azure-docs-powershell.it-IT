---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521460"
---
# <span data-ttu-id="01c7e-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="01c7e-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="01c7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="01c7e-103">Rimuove una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="01c7e-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01c7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01c7e-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01c7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="01c7e-106">Il cmdlet **Remove-AzureRmAutomationConnection** rimuove una connessione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="01c7e-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="01c7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01c7e-107">EXAMPLES</span></span>

### <span data-ttu-id="01c7e-108">Esempio 1: rimuovere una connessione</span><span class="sxs-lookup"><span data-stu-id="01c7e-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="01c7e-109">Questo comando rimuove un certificato denominato ContosoConnection nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="01c7e-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="01c7e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="01c7e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01c7e-111">-AutomationAccountName</span></span>
<span data-ttu-id="01c7e-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="01c7e-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c7e-113">-DefaultProfile</span></span>
<span data-ttu-id="01c7e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="01c7e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c7e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="01c7e-115">-Force</span></span>
<span data-ttu-id="01c7e-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="01c7e-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c7e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="01c7e-117">-Name</span></span>
<span data-ttu-id="01c7e-118">Specifica il nome della connessione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01c7e-118">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c7e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c7e-119">-ResourceGroupName</span></span>
<span data-ttu-id="01c7e-120">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="01c7e-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c7e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01c7e-121">-Confirm</span></span>
<span data-ttu-id="01c7e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01c7e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c7e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c7e-123">-WhatIf</span></span>
<span data-ttu-id="01c7e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01c7e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c7e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01c7e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c7e-126">CommonParameters</span></span>
<span data-ttu-id="01c7e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c7e-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c7e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c7e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01c7e-129">INPUTS</span></span>

### <span data-ttu-id="01c7e-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="01c7e-130">None</span></span>
<span data-ttu-id="01c7e-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="01c7e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01c7e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01c7e-132">OUTPUTS</span></span>

## <span data-ttu-id="01c7e-133">Note</span><span class="sxs-lookup"><span data-stu-id="01c7e-133">NOTES</span></span>

## <span data-ttu-id="01c7e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01c7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="01c7e-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="01c7e-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="01c7e-136">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="01c7e-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


