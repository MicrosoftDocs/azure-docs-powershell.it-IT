---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 9268d1859f42b7849f8e4a61ae39aa4b68994e4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516560"
---
# <span data-ttu-id="dbae3-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbae3-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="dbae3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbae3-102">SYNOPSIS</span></span>
<span data-ttu-id="dbae3-103">Rimuove un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbae3-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbae3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbae3-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbae3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbae3-105">DESCRIPTION</span></span>
<span data-ttu-id="dbae3-106">Il cmdlet **Remove-AzureRmIntegrationAccountPartner** rimuove un partner dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbae3-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="dbae3-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="dbae3-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="dbae3-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="dbae3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dbae3-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="dbae3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dbae3-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="dbae3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dbae3-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="dbae3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dbae3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbae3-112">EXAMPLES</span></span>

### <span data-ttu-id="dbae3-113">Esempio 1: rimuovere un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="dbae3-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="dbae3-114">Questo comando rimuove il partner account di integrazione denominato IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="dbae3-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="dbae3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbae3-115">PARAMETERS</span></span>

### <span data-ttu-id="dbae3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbae3-116">-DefaultProfile</span></span>
<span data-ttu-id="dbae3-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dbae3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbae3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dbae3-118">-Force</span></span>
<span data-ttu-id="dbae3-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dbae3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbae3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbae3-120">-Name</span></span>
<span data-ttu-id="dbae3-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbae3-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="dbae3-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="dbae3-122">-PartnerName</span></span>
<span data-ttu-id="dbae3-123">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbae3-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="dbae3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbae3-124">-ResourceGroupName</span></span>
<span data-ttu-id="dbae3-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbae3-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dbae3-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dbae3-126">-Confirm</span></span>
<span data-ttu-id="dbae3-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbae3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbae3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbae3-128">-WhatIf</span></span>
<span data-ttu-id="dbae3-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbae3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbae3-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbae3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbae3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbae3-131">CommonParameters</span></span>
<span data-ttu-id="dbae3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbae3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbae3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbae3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbae3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbae3-134">INPUTS</span></span>

### <span data-ttu-id="dbae3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dbae3-135">System.String</span></span>

## <span data-ttu-id="dbae3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbae3-136">OUTPUTS</span></span>

### <span data-ttu-id="dbae3-137">System. void</span><span class="sxs-lookup"><span data-stu-id="dbae3-137">System.Void</span></span>

## <span data-ttu-id="dbae3-138">Note</span><span class="sxs-lookup"><span data-stu-id="dbae3-138">NOTES</span></span>

## <span data-ttu-id="dbae3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbae3-139">RELATED LINKS</span></span>

[<span data-ttu-id="dbae3-140">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbae3-140">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="dbae3-141">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbae3-141">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="dbae3-142">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="dbae3-142">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


