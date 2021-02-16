---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: edd50a72ed0614cf7c71dfbde9f487e8fe632d85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187559"
---
# <span data-ttu-id="a5830-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a5830-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="a5830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5830-102">SYNOPSIS</span></span>
<span data-ttu-id="a5830-103">Modifica un partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="a5830-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5830-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5830-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5830-105">DESCRIPTION</span></span>
<span data-ttu-id="a5830-106">Il cmdlet **Set-AzIntegrationAccountPartner modifica** un partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="a5830-107">Questo cmdlet restituisce un oggetto che rappresenta il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="a5830-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="a5830-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="a5830-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="a5830-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a5830-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="a5830-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a5830-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a5830-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a5830-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="a5830-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a5830-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5830-113">EXAMPLES</span></span>

### <span data-ttu-id="a5830-114">Esempio 1: Modificare un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a5830-114">Example 1: Modify an integration account partner</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="a5830-115">Questo comando modifica il partner dell'account di integrazione denominato IntegrationAccountPartner22 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a5830-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="a5830-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a5830-116">Example 2</span></span>

<span data-ttu-id="a5830-117">Modifica un partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-117">Modifies an integration account partner.</span></span> <span data-ttu-id="a5830-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="a5830-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="a5830-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5830-119">PARAMETERS</span></span>

### <span data-ttu-id="a5830-120">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="a5830-120">-BusinessIdentities</span></span>
<span data-ttu-id="a5830-121">Specifica le identità aziendali per il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="a5830-122">Specificare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a5830-122">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5830-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5830-123">-DefaultProfile</span></span>
<span data-ttu-id="a5830-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a5830-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5830-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a5830-125">-Force</span></span>
<span data-ttu-id="a5830-126">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="a5830-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5830-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a5830-127">-Metadata</span></span>
<span data-ttu-id="a5830-128">Specifica un oggetto metadati per il partner.</span><span class="sxs-lookup"><span data-stu-id="a5830-128">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5830-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a5830-129">-Name</span></span>
<span data-ttu-id="a5830-130">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-130">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5830-131">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="a5830-131">-PartnerName</span></span>
<span data-ttu-id="a5830-132">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="a5830-133">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="a5830-133">-PartnerType</span></span>
<span data-ttu-id="a5830-134">Specifica il tipo di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a5830-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="a5830-135">Questo parametro supporta il tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="a5830-135">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5830-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5830-136">-ResourceGroupName</span></span>
<span data-ttu-id="a5830-137">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5830-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a5830-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5830-138">-Confirm</span></span>
<span data-ttu-id="a5830-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5830-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5830-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5830-140">-WhatIf</span></span>
<span data-ttu-id="a5830-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5830-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5830-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5830-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5830-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5830-143">CommonParameters</span></span>
<span data-ttu-id="a5830-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5830-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5830-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5830-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5830-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5830-146">INPUTS</span></span>

### <span data-ttu-id="a5830-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a5830-147">System.String</span></span>

## <span data-ttu-id="a5830-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5830-148">OUTPUTS</span></span>

### <span data-ttu-id="a5830-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a5830-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="a5830-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5830-150">NOTES</span></span>

## <span data-ttu-id="a5830-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5830-151">RELATED LINKS</span></span>

[<span data-ttu-id="a5830-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a5830-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="a5830-153">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a5830-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="a5830-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a5830-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


