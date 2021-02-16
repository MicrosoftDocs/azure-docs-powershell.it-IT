---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194214"
---
# <span data-ttu-id="8df74-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8df74-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="8df74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df74-102">SYNOPSIS</span></span>
<span data-ttu-id="8df74-103">Rimuove il contratto di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8df74-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="8df74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8df74-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df74-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8df74-105">DESCRIPTION</span></span>
<span data-ttu-id="8df74-106">Il cmdlet **Remove-AzIntegrationAccountAgreement** rimuove un contratto di account di integrazione da un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="8df74-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="8df74-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="8df74-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="8df74-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="8df74-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8df74-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="8df74-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8df74-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="8df74-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8df74-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="8df74-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8df74-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8df74-112">EXAMPLES</span></span>

### <span data-ttu-id="8df74-113">Esempio 1: Rimuovere un contratto di account di integrazione in base al nome</span><span class="sxs-lookup"><span data-stu-id="8df74-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="8df74-114">Questo comando rimuove il contratto di account di integrazione denominato IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="8df74-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="8df74-115">Il comando non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8df74-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8df74-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8df74-116">PARAMETERS</span></span>

### <span data-ttu-id="8df74-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="8df74-117">-AgreementName</span></span>
<span data-ttu-id="8df74-118">Specifica il nome del contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8df74-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="8df74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df74-119">-DefaultProfile</span></span>
<span data-ttu-id="8df74-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8df74-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8df74-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8df74-121">-Force</span></span>
<span data-ttu-id="8df74-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="8df74-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8df74-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8df74-123">-Name</span></span>
<span data-ttu-id="8df74-124">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8df74-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="8df74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df74-125">-ResourceGroupName</span></span>
<span data-ttu-id="8df74-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8df74-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8df74-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8df74-127">-Confirm</span></span>
<span data-ttu-id="8df74-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8df74-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df74-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df74-129">-WhatIf</span></span>
<span data-ttu-id="8df74-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8df74-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df74-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8df74-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df74-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df74-132">CommonParameters</span></span>
<span data-ttu-id="8df74-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df74-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df74-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df74-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df74-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="8df74-135">INPUTS</span></span>

### <span data-ttu-id="8df74-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8df74-136">System.String</span></span>

## <span data-ttu-id="8df74-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8df74-137">OUTPUTS</span></span>

### <span data-ttu-id="8df74-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="8df74-138">System.Void</span></span>

## <span data-ttu-id="8df74-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="8df74-139">NOTES</span></span>

## <span data-ttu-id="8df74-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8df74-140">RELATED LINKS</span></span>

[<span data-ttu-id="8df74-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8df74-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="8df74-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8df74-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="8df74-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8df74-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


