---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: e8bf71ec58273e89ad8f32e65c9c110205239dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521430"
---
# <span data-ttu-id="df3e8-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="df3e8-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="df3e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="df3e8-103">Modifica il partner di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df3e8-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df3e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df3e8-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df3e8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df3e8-105">DESCRIPTION</span></span>
<span data-ttu-id="df3e8-106">Il cmdlet **set-AzureRmIntegrationAccountPartner** modifica un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df3e8-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="df3e8-107">Questo cmdlet restituisce un oggetto che rappresenta il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df3e8-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="df3e8-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="df3e8-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="df3e8-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="df3e8-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="df3e8-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="df3e8-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="df3e8-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="df3e8-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="df3e8-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="df3e8-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="df3e8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df3e8-113">EXAMPLES</span></span>

### <span data-ttu-id="df3e8-114">Esempio 1: modificare un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="df3e8-114">Example 1: Modify an integration account partner</span></span>
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

<span data-ttu-id="df3e8-115">Questo comando modifica il partner dell'account di integrazione denominato IntegrationAccountPartner22 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="df3e8-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="df3e8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df3e8-116">PARAMETERS</span></span>

### <span data-ttu-id="df3e8-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="df3e8-117">-BusinessIdentities</span></span>
<span data-ttu-id="df3e8-118">Specifica le identità aziendali per il partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df3e8-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="df3e8-119">Specificare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="df3e8-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="df3e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df3e8-120">-DefaultProfile</span></span>
<span data-ttu-id="df3e8-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="df3e8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df3e8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="df3e8-122">-Force</span></span>
<span data-ttu-id="df3e8-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="df3e8-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df3e8-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="df3e8-124">-Metadata</span></span>
<span data-ttu-id="df3e8-125">Specifica un oggetto Metadata per il partner.</span><span class="sxs-lookup"><span data-stu-id="df3e8-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="df3e8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="df3e8-126">-Name</span></span>
<span data-ttu-id="df3e8-127">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df3e8-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="df3e8-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="df3e8-128">-PartnerName</span></span>
<span data-ttu-id="df3e8-129">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df3e8-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="df3e8-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="df3e8-130">-PartnerType</span></span>
<span data-ttu-id="df3e8-131">Specifica il tipo di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df3e8-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="df3e8-132">Questo parametro supporta il tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="df3e8-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="df3e8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df3e8-133">-ResourceGroupName</span></span>
<span data-ttu-id="df3e8-134">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df3e8-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="df3e8-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df3e8-135">-Confirm</span></span>
<span data-ttu-id="df3e8-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df3e8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df3e8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df3e8-137">-WhatIf</span></span>
<span data-ttu-id="df3e8-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df3e8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df3e8-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df3e8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df3e8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3e8-140">CommonParameters</span></span>
<span data-ttu-id="df3e8-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df3e8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3e8-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df3e8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3e8-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df3e8-143">INPUTS</span></span>

### <span data-ttu-id="df3e8-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="df3e8-144">None</span></span>
<span data-ttu-id="df3e8-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="df3e8-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df3e8-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df3e8-146">OUTPUTS</span></span>

### <span data-ttu-id="df3e8-147">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="df3e8-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="df3e8-148">Note</span><span class="sxs-lookup"><span data-stu-id="df3e8-148">NOTES</span></span>

## <span data-ttu-id="df3e8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df3e8-149">RELATED LINKS</span></span>

[<span data-ttu-id="df3e8-150">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="df3e8-150">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="df3e8-151">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="df3e8-151">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="df3e8-152">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="df3e8-152">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


