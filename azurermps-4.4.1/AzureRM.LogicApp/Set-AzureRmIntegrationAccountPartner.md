---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 13b82cbc7b1f83c441f1211f6ebe7aa1f8c59ea5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687167"
---
# <span data-ttu-id="98a1a-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="98a1a-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="98a1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="98a1a-103">Modifica il partner di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="98a1a-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98a1a-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98a1a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="98a1a-106">Il cmdlet **set-AzureRmIntegrationAccountPartner** modifica un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="98a1a-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="98a1a-107">Questo cmdlet restituisce un oggetto che rappresenta il partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="98a1a-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="98a1a-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="98a1a-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="98a1a-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="98a1a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="98a1a-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="98a1a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="98a1a-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="98a1a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="98a1a-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="98a1a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="98a1a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98a1a-113">EXAMPLES</span></span>

### <span data-ttu-id="98a1a-114">Esempio 1: modificare un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="98a1a-114">Example 1: Modify an integration account partner</span></span>
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

<span data-ttu-id="98a1a-115">Questo comando modifica il partner dell'account di integrazione denominato IntegrationAccountPartner22 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="98a1a-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="98a1a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98a1a-116">PARAMETERS</span></span>

### <span data-ttu-id="98a1a-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="98a1a-117">-BusinessIdentities</span></span>
<span data-ttu-id="98a1a-118">Specifica le identità aziendali per il partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="98a1a-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="98a1a-119">Specificare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="98a1a-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="98a1a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="98a1a-120">-Force</span></span>
<span data-ttu-id="98a1a-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="98a1a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98a1a-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="98a1a-122">-Metadata</span></span>
<span data-ttu-id="98a1a-123">Specifica un oggetto Metadata per il partner.</span><span class="sxs-lookup"><span data-stu-id="98a1a-123">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="98a1a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="98a1a-124">-Name</span></span>
<span data-ttu-id="98a1a-125">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="98a1a-125">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="98a1a-126">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="98a1a-126">-PartnerName</span></span>
<span data-ttu-id="98a1a-127">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="98a1a-127">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="98a1a-128">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="98a1a-128">-PartnerType</span></span>
<span data-ttu-id="98a1a-129">Specifica il tipo di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="98a1a-129">Specifies the type of the integration account.</span></span>
<span data-ttu-id="98a1a-130">Questo parametro supporta il tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="98a1a-130">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="98a1a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a1a-131">-ResourceGroupName</span></span>
<span data-ttu-id="98a1a-132">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="98a1a-132">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="98a1a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98a1a-133">-Confirm</span></span>
<span data-ttu-id="98a1a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98a1a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98a1a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98a1a-135">-WhatIf</span></span>
<span data-ttu-id="98a1a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98a1a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98a1a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98a1a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98a1a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a1a-138">-DefaultProfile</span></span>
<span data-ttu-id="98a1a-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98a1a-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98a1a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a1a-140">CommonParameters</span></span>
<span data-ttu-id="98a1a-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a1a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a1a-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a1a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a1a-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98a1a-143">INPUTS</span></span>

## <span data-ttu-id="98a1a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98a1a-144">OUTPUTS</span></span>

### <span data-ttu-id="98a1a-145">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="98a1a-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="98a1a-146">Note</span><span class="sxs-lookup"><span data-stu-id="98a1a-146">NOTES</span></span>

## <span data-ttu-id="98a1a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98a1a-147">RELATED LINKS</span></span>

[<span data-ttu-id="98a1a-148">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="98a1a-148">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="98a1a-149">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="98a1a-149">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="98a1a-150">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="98a1a-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

