---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: ca7e043d8205800322469a59cea6c17ceb96eff6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687828"
---
# <span data-ttu-id="598ef-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="598ef-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="598ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="598ef-102">SYNOPSIS</span></span>
<span data-ttu-id="598ef-103">Modifica il partner di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="598ef-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="598ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="598ef-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="598ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="598ef-105">DESCRIPTION</span></span>
<span data-ttu-id="598ef-106">Il cmdlet **set-AzureRmIntegrationAccountPartner** modifica un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="598ef-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="598ef-107">Questo cmdlet restituisce un oggetto che rappresenta il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="598ef-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="598ef-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="598ef-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="598ef-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="598ef-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="598ef-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="598ef-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="598ef-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="598ef-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="598ef-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="598ef-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="598ef-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="598ef-113">EXAMPLES</span></span>

### <span data-ttu-id="598ef-114">Esempio 1: modificare un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="598ef-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="598ef-115">Questo comando modifica il partner dell'account di integrazione denominato IntegrationAccountPartner22 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="598ef-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="598ef-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="598ef-116">PARAMETERS</span></span>

### <span data-ttu-id="598ef-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="598ef-117">-BusinessIdentities</span></span>
<span data-ttu-id="598ef-118">Specifica le identità aziendali per il partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="598ef-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="598ef-119">Specificare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="598ef-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="598ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598ef-120">-DefaultProfile</span></span>
<span data-ttu-id="598ef-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="598ef-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="598ef-122">-Force</span><span class="sxs-lookup"><span data-stu-id="598ef-122">-Force</span></span>
<span data-ttu-id="598ef-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="598ef-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="598ef-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="598ef-124">-Metadata</span></span>
<span data-ttu-id="598ef-125">Specifica un oggetto Metadata per il partner.</span><span class="sxs-lookup"><span data-stu-id="598ef-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="598ef-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="598ef-126">-Name</span></span>
<span data-ttu-id="598ef-127">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="598ef-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="598ef-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="598ef-128">-PartnerName</span></span>
<span data-ttu-id="598ef-129">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="598ef-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="598ef-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="598ef-130">-PartnerType</span></span>
<span data-ttu-id="598ef-131">Specifica il tipo di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="598ef-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="598ef-132">Questo parametro supporta il tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="598ef-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="598ef-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598ef-133">-ResourceGroupName</span></span>
<span data-ttu-id="598ef-134">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="598ef-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="598ef-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="598ef-135">-Confirm</span></span>
<span data-ttu-id="598ef-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="598ef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="598ef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="598ef-137">-WhatIf</span></span>
<span data-ttu-id="598ef-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="598ef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="598ef-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="598ef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="598ef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598ef-140">CommonParameters</span></span>
<span data-ttu-id="598ef-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="598ef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598ef-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="598ef-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598ef-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="598ef-143">INPUTS</span></span>

### <span data-ttu-id="598ef-144">System. String</span><span class="sxs-lookup"><span data-stu-id="598ef-144">System.String</span></span>

## <span data-ttu-id="598ef-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="598ef-145">OUTPUTS</span></span>

### <span data-ttu-id="598ef-146">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="598ef-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="598ef-147">Note</span><span class="sxs-lookup"><span data-stu-id="598ef-147">NOTES</span></span>

## <span data-ttu-id="598ef-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="598ef-148">RELATED LINKS</span></span>

[<span data-ttu-id="598ef-149">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="598ef-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="598ef-150">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="598ef-150">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="598ef-151">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="598ef-151">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


