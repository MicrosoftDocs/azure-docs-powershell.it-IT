---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: bbd64f1e6df016efe0bdd22bb0ae848c79566edf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203709"
---
# <span data-ttu-id="1f44d-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1f44d-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="1f44d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f44d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f44d-103">Crea un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f44d-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="1f44d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f44d-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f44d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f44d-105">DESCRIPTION</span></span>
<span data-ttu-id="1f44d-106">Il cmdlet **New-AzIntegrationAccountPartner crea** un partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f44d-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="1f44d-107">Questo cmdlet restituisce un oggetto che rappresenta il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f44d-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="1f44d-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome del partner e le identità del partner.</span><span class="sxs-lookup"><span data-stu-id="1f44d-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="1f44d-109">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri di modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="1f44d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="1f44d-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="1f44d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1f44d-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="1f44d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1f44d-112">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="1f44d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1f44d-113">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="1f44d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1f44d-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f44d-114">EXAMPLES</span></span>

### <span data-ttu-id="1f44d-115">Esempio 1: Creare un partner account di integrazione</span><span class="sxs-lookup"><span data-stu-id="1f44d-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="1f44d-116">Questo comando crea il partner dell'account di integrazione denominato IntegrationAccountPartner22 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1f44d-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="1f44d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f44d-117">PARAMETERS</span></span>

### <span data-ttu-id="1f44d-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="1f44d-118">-BusinessIdentities</span></span>
<span data-ttu-id="1f44d-119">Specifica le identità aziendali per il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f44d-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="1f44d-120">Specificare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1f44d-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f44d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f44d-121">-DefaultProfile</span></span>
<span data-ttu-id="1f44d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1f44d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f44d-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1f44d-123">-Metadata</span></span>
<span data-ttu-id="1f44d-124">Specifica un oggetto metadati per il partner.</span><span class="sxs-lookup"><span data-stu-id="1f44d-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="1f44d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1f44d-125">-Name</span></span>
<span data-ttu-id="1f44d-126">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f44d-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="1f44d-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="1f44d-127">-PartnerName</span></span>
<span data-ttu-id="1f44d-128">Specifica un nome per il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f44d-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="1f44d-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="1f44d-129">-PartnerType</span></span>
<span data-ttu-id="1f44d-130">Specifica il tipo di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f44d-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="1f44d-131">Questo parametro supporta il tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="1f44d-131">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="1f44d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f44d-132">-ResourceGroupName</span></span>
<span data-ttu-id="1f44d-133">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f44d-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1f44d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f44d-134">-Confirm</span></span>
<span data-ttu-id="1f44d-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f44d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f44d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f44d-136">-WhatIf</span></span>
<span data-ttu-id="1f44d-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f44d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f44d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f44d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f44d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f44d-139">CommonParameters</span></span>
<span data-ttu-id="1f44d-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f44d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f44d-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f44d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f44d-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f44d-142">INPUTS</span></span>

### <span data-ttu-id="1f44d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1f44d-143">System.String</span></span>

## <span data-ttu-id="1f44d-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f44d-144">OUTPUTS</span></span>

### <span data-ttu-id="1f44d-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1f44d-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="1f44d-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f44d-146">NOTES</span></span>

## <span data-ttu-id="1f44d-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f44d-147">RELATED LINKS</span></span>

[<span data-ttu-id="1f44d-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1f44d-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="1f44d-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1f44d-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="1f44d-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1f44d-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


