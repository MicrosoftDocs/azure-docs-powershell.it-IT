---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: ac66c1d28c53224fedb18000db86557c8290d41a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018382"
---
# <span data-ttu-id="cdaee-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdaee-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="cdaee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdaee-102">SYNOPSIS</span></span>
<span data-ttu-id="cdaee-103">Modifica il partner di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdaee-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="cdaee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdaee-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdaee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdaee-105">DESCRIPTION</span></span>
<span data-ttu-id="cdaee-106">Il cmdlet **set-AzIntegrationAccountPartner** modifica un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdaee-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="cdaee-107">Questo cmdlet restituisce un oggetto che rappresenta il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdaee-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="cdaee-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="cdaee-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="cdaee-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="cdaee-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cdaee-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="cdaee-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cdaee-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="cdaee-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cdaee-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="cdaee-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cdaee-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdaee-113">EXAMPLES</span></span>

### <span data-ttu-id="cdaee-114">Esempio 1: modificare un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="cdaee-114">Example 1: Modify an integration account partner</span></span>
```
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

<span data-ttu-id="cdaee-115">Questo comando modifica il partner dell'account di integrazione denominato IntegrationAccountPartner22 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="cdaee-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="cdaee-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdaee-116">PARAMETERS</span></span>

### <span data-ttu-id="cdaee-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="cdaee-117">-BusinessIdentities</span></span>
<span data-ttu-id="cdaee-118">Specifica le identità aziendali per il partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdaee-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="cdaee-119">Specificare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cdaee-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="cdaee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdaee-120">-DefaultProfile</span></span>
<span data-ttu-id="cdaee-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cdaee-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdaee-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cdaee-122">-Force</span></span>
<span data-ttu-id="cdaee-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cdaee-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdaee-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cdaee-124">-Metadata</span></span>
<span data-ttu-id="cdaee-125">Specifica un oggetto Metadata per il partner.</span><span class="sxs-lookup"><span data-stu-id="cdaee-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="cdaee-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdaee-126">-Name</span></span>
<span data-ttu-id="cdaee-127">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdaee-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="cdaee-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="cdaee-128">-PartnerName</span></span>
<span data-ttu-id="cdaee-129">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdaee-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="cdaee-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="cdaee-130">-PartnerType</span></span>
<span data-ttu-id="cdaee-131">Specifica il tipo di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdaee-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="cdaee-132">Questo parametro supporta il tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="cdaee-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="cdaee-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdaee-133">-ResourceGroupName</span></span>
<span data-ttu-id="cdaee-134">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdaee-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cdaee-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdaee-135">-Confirm</span></span>
<span data-ttu-id="cdaee-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdaee-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdaee-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdaee-137">-WhatIf</span></span>
<span data-ttu-id="cdaee-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdaee-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdaee-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdaee-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdaee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdaee-140">CommonParameters</span></span>
<span data-ttu-id="cdaee-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdaee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdaee-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdaee-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdaee-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdaee-143">INPUTS</span></span>

### <span data-ttu-id="cdaee-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cdaee-144">System.String</span></span>

## <span data-ttu-id="cdaee-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdaee-145">OUTPUTS</span></span>

### <span data-ttu-id="cdaee-146">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdaee-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="cdaee-147">Note</span><span class="sxs-lookup"><span data-stu-id="cdaee-147">NOTES</span></span>

## <span data-ttu-id="cdaee-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdaee-148">RELATED LINKS</span></span>

[<span data-ttu-id="cdaee-149">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdaee-149">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="cdaee-150">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdaee-150">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="cdaee-151">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdaee-151">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


