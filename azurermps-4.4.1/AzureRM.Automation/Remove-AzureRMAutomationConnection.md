---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: aade8dec765a7336292e0350d098417e29d0e360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518395"
---
# <span data-ttu-id="dd242-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dd242-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="dd242-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd242-102">SYNOPSIS</span></span>
<span data-ttu-id="dd242-103">Rimuove una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="dd242-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd242-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd242-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd242-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd242-105">DESCRIPTION</span></span>
<span data-ttu-id="dd242-106">Il cmdlet **Remove-AzureRmAutomationConnection** rimuove una connessione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dd242-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="dd242-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd242-107">EXAMPLES</span></span>

### <span data-ttu-id="dd242-108">Esempio 1: rimuovere una connessione</span><span class="sxs-lookup"><span data-stu-id="dd242-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dd242-109">Questo comando rimuove un certificato denominato ContosoConnection nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dd242-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dd242-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd242-110">PARAMETERS</span></span>

### <span data-ttu-id="dd242-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd242-111">-AutomationAccountName</span></span>
<span data-ttu-id="dd242-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="dd242-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="dd242-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dd242-113">-Force</span></span>
<span data-ttu-id="dd242-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="dd242-114">ps_force</span></span>

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

### <span data-ttu-id="dd242-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd242-115">-Name</span></span>
<span data-ttu-id="dd242-116">Specifica il nome della connessione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd242-116">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd242-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd242-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd242-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una connessione.</span><span class="sxs-lookup"><span data-stu-id="dd242-118">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="dd242-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd242-119">-Confirm</span></span>
<span data-ttu-id="dd242-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd242-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd242-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd242-121">-WhatIf</span></span>
<span data-ttu-id="dd242-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd242-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd242-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd242-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd242-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd242-124">-DefaultProfile</span></span>
<span data-ttu-id="dd242-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd242-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd242-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd242-126">CommonParameters</span></span>
<span data-ttu-id="dd242-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd242-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd242-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd242-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd242-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd242-129">INPUTS</span></span>

## <span data-ttu-id="dd242-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd242-130">OUTPUTS</span></span>

## <span data-ttu-id="dd242-131">Note</span><span class="sxs-lookup"><span data-stu-id="dd242-131">NOTES</span></span>

## <span data-ttu-id="dd242-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd242-132">RELATED LINKS</span></span>

[<span data-ttu-id="dd242-133">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dd242-133">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="dd242-134">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dd242-134">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


