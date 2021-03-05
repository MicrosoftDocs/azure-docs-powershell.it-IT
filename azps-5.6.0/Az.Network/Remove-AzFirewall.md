---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 4be419ab76180174fd6132335822c361008ec872
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993774"
---
# <span data-ttu-id="d163d-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d163d-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="d163d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d163d-102">SYNOPSIS</span></span>
<span data-ttu-id="d163d-103">Rimuovere un firewall.</span><span class="sxs-lookup"><span data-stu-id="d163d-103">Remove a Firewall.</span></span>

## <span data-ttu-id="d163d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d163d-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d163d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d163d-105">DESCRIPTION</span></span>
<span data-ttu-id="d163d-106">Il cmdlet **Remove-AzFirewall** rimuove un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="d163d-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="d163d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d163d-107">EXAMPLES</span></span>

### <span data-ttu-id="d163d-108">Esempio 1: Creare ed eliminare un firewall</span><span class="sxs-lookup"><span data-stu-id="d163d-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="d163d-109">Questo esempio crea un firewall e quindi lo elimina.</span><span class="sxs-lookup"><span data-stu-id="d163d-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="d163d-110">Per eliminare la richiesta quando si elimina il firewall, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="d163d-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="d163d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d163d-111">PARAMETERS</span></span>

### <span data-ttu-id="d163d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d163d-112">-AsJob</span></span>
<span data-ttu-id="d163d-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d163d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d163d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d163d-114">-DefaultProfile</span></span>
<span data-ttu-id="d163d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d163d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d163d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d163d-116">-Force</span></span>
<span data-ttu-id="d163d-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="d163d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d163d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d163d-118">-Name</span></span>
<span data-ttu-id="d163d-119">Specifica il nome del firewall rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d163d-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d163d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d163d-120">-PassThru</span></span>
<span data-ttu-id="d163d-121">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d163d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d163d-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d163d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d163d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d163d-123">-ResourceGroupName</span></span>
<span data-ttu-id="d163d-124">Specifica il nome del gruppo di risorse che contiene il firewall rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d163d-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d163d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d163d-125">-Confirm</span></span>
<span data-ttu-id="d163d-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d163d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d163d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d163d-127">-WhatIf</span></span>
<span data-ttu-id="d163d-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d163d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d163d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d163d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d163d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d163d-130">CommonParameters</span></span>
<span data-ttu-id="d163d-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d163d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d163d-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d163d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d163d-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="d163d-133">INPUTS</span></span>

### <span data-ttu-id="d163d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d163d-134">System.String</span></span>

## <span data-ttu-id="d163d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d163d-135">OUTPUTS</span></span>

### <span data-ttu-id="d163d-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d163d-136">System.Boolean</span></span>

## <span data-ttu-id="d163d-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="d163d-137">NOTES</span></span>

## <span data-ttu-id="d163d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d163d-138">RELATED LINKS</span></span>

[<span data-ttu-id="d163d-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d163d-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d163d-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d163d-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d163d-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d163d-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
