---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 470a400721d911e09c7bed4e51eb6cef39a1dafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518087"
---
# <span data-ttu-id="8eaed-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8eaed-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="8eaed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8eaed-102">SYNOPSIS</span></span>
<span data-ttu-id="8eaed-103">Crea un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eaed-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eaed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8eaed-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eaed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8eaed-105">DESCRIPTION</span></span>
<span data-ttu-id="8eaed-106">Il cmdlet **New-AzureRmIntegrationAccountPartner** crea un partner per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eaed-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="8eaed-107">Questo cmdlet restituisce un oggetto che rappresenta il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eaed-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="8eaed-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome del partner e le identità dei partner.</span><span class="sxs-lookup"><span data-stu-id="8eaed-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="8eaed-109">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="8eaed-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="8eaed-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="8eaed-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8eaed-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="8eaed-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8eaed-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="8eaed-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8eaed-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="8eaed-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8eaed-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8eaed-114">EXAMPLES</span></span>

### <span data-ttu-id="8eaed-115">Esempio 1: creare un partner per l'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="8eaed-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="8eaed-116">Questo comando crea il partner dell'account di integrazione denominato IntegrationAccountPartner22 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8eaed-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="8eaed-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8eaed-117">PARAMETERS</span></span>

### <span data-ttu-id="8eaed-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="8eaed-118">-BusinessIdentities</span></span>
<span data-ttu-id="8eaed-119">Specifica le identità aziendali per il partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eaed-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="8eaed-120">Specificare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8eaed-120">Specify a hash table.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eaed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eaed-121">-DefaultProfile</span></span>
<span data-ttu-id="8eaed-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8eaed-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8eaed-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8eaed-123">-Metadata</span></span>
<span data-ttu-id="8eaed-124">Specifica un oggetto Metadata per il partner.</span><span class="sxs-lookup"><span data-stu-id="8eaed-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eaed-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8eaed-125">-Name</span></span>
<span data-ttu-id="8eaed-126">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eaed-126">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eaed-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="8eaed-127">-PartnerName</span></span>
<span data-ttu-id="8eaed-128">Specifica un nome per il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eaed-128">Specifies a name for the integration account partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eaed-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="8eaed-129">-PartnerType</span></span>
<span data-ttu-id="8eaed-130">Specifica il tipo di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eaed-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="8eaed-131">Questo parametro supporta il tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="8eaed-131">This parameter supports the type B2B.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eaed-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eaed-132">-ResourceGroupName</span></span>
<span data-ttu-id="8eaed-133">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8eaed-133">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eaed-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8eaed-134">-Confirm</span></span>
<span data-ttu-id="8eaed-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eaed-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eaed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eaed-136">-WhatIf</span></span>
<span data-ttu-id="8eaed-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8eaed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eaed-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8eaed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eaed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eaed-139">CommonParameters</span></span>
<span data-ttu-id="8eaed-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eaed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eaed-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eaed-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eaed-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8eaed-142">INPUTS</span></span>

### <span data-ttu-id="8eaed-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8eaed-143">None</span></span>
<span data-ttu-id="8eaed-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8eaed-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8eaed-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8eaed-145">OUTPUTS</span></span>

### <span data-ttu-id="8eaed-146">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8eaed-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="8eaed-147">Note</span><span class="sxs-lookup"><span data-stu-id="8eaed-147">NOTES</span></span>

## <span data-ttu-id="8eaed-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8eaed-148">RELATED LINKS</span></span>

[<span data-ttu-id="8eaed-149">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8eaed-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="8eaed-150">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8eaed-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="8eaed-151">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8eaed-151">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


