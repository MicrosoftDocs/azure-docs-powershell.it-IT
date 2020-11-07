---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a1a34ca669b12ee815655531c33b6cdba519016c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688166"
---
# <span data-ttu-id="9e07f-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9e07f-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="9e07f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e07f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e07f-103">Rimuove uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9e07f-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e07f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e07f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e07f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e07f-105">DESCRIPTION</span></span>
<span data-ttu-id="9e07f-106">Il cmdlet **Remove-AzureRmIntegrationAccountSchema** rimuove uno schema di account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e07f-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="9e07f-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="9e07f-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="9e07f-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="9e07f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9e07f-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="9e07f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9e07f-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="9e07f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9e07f-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="9e07f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9e07f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e07f-112">EXAMPLES</span></span>

### <span data-ttu-id="9e07f-113">Esempio 1: rimuovere uno schema dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="9e07f-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="9e07f-114">Questo comando rimuove uno schema di account di integrazione denominato IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="9e07f-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="9e07f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e07f-115">PARAMETERS</span></span>

### <span data-ttu-id="9e07f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e07f-116">-DefaultProfile</span></span>
<span data-ttu-id="9e07f-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9e07f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e07f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9e07f-118">-Force</span></span>
<span data-ttu-id="9e07f-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9e07f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e07f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e07f-120">-Name</span></span>
<span data-ttu-id="9e07f-121">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9e07f-121">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e07f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e07f-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e07f-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e07f-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9e07f-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9e07f-124">-SchemaName</span></span>
<span data-ttu-id="9e07f-125">Specifica il nome di uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9e07f-125">Specifies the name of an integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e07f-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e07f-126">-Confirm</span></span>
<span data-ttu-id="9e07f-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e07f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e07f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e07f-128">-WhatIf</span></span>
<span data-ttu-id="9e07f-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e07f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e07f-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e07f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e07f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e07f-131">CommonParameters</span></span>
<span data-ttu-id="9e07f-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e07f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e07f-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e07f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e07f-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e07f-134">INPUTS</span></span>

### <span data-ttu-id="9e07f-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9e07f-135">None</span></span>
<span data-ttu-id="9e07f-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9e07f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e07f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e07f-137">OUTPUTS</span></span>

## <span data-ttu-id="9e07f-138">Note</span><span class="sxs-lookup"><span data-stu-id="9e07f-138">NOTES</span></span>

## <span data-ttu-id="9e07f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e07f-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e07f-140">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9e07f-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="9e07f-141">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9e07f-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="9e07f-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9e07f-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)

