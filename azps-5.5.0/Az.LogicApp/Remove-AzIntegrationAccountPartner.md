---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185151"
---
# <span data-ttu-id="2fd11-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2fd11-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="2fd11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fd11-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd11-103">Rimuove un partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2fd11-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="2fd11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fd11-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fd11-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2fd11-105">DESCRIPTION</span></span>
<span data-ttu-id="2fd11-106">Il cmdlet **Remove-AzIntegrationAccountPartner** rimuove un partner dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2fd11-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="2fd11-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="2fd11-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="2fd11-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="2fd11-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2fd11-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="2fd11-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2fd11-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="2fd11-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2fd11-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="2fd11-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2fd11-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fd11-112">EXAMPLES</span></span>

### <span data-ttu-id="2fd11-113">Esempio 1: Rimuovere un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2fd11-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="2fd11-114">Questo comando rimuove il partner dell'account di integrazione denominato IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="2fd11-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="2fd11-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fd11-115">PARAMETERS</span></span>

### <span data-ttu-id="2fd11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd11-116">-DefaultProfile</span></span>
<span data-ttu-id="2fd11-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="2fd11-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fd11-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2fd11-118">-Force</span></span>
<span data-ttu-id="2fd11-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="2fd11-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fd11-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2fd11-120">-Name</span></span>
<span data-ttu-id="2fd11-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2fd11-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="2fd11-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="2fd11-122">-PartnerName</span></span>
<span data-ttu-id="2fd11-123">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2fd11-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="2fd11-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd11-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fd11-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2fd11-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2fd11-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fd11-126">-Confirm</span></span>
<span data-ttu-id="2fd11-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fd11-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd11-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd11-128">-WhatIf</span></span>
<span data-ttu-id="2fd11-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fd11-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd11-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fd11-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd11-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd11-131">CommonParameters</span></span>
<span data-ttu-id="2fd11-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fd11-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd11-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd11-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd11-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2fd11-134">INPUTS</span></span>

### <span data-ttu-id="2fd11-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2fd11-135">System.String</span></span>

## <span data-ttu-id="2fd11-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fd11-136">OUTPUTS</span></span>

### <span data-ttu-id="2fd11-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="2fd11-137">System.Void</span></span>

## <span data-ttu-id="2fd11-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="2fd11-138">NOTES</span></span>

## <span data-ttu-id="2fd11-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fd11-139">RELATED LINKS</span></span>

[<span data-ttu-id="2fd11-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2fd11-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="2fd11-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2fd11-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="2fd11-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2fd11-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


