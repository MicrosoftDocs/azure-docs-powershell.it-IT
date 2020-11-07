---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 7342601bba3c963131728f02773cb3b84e917bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673989"
---
# <span data-ttu-id="15b58-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="15b58-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="15b58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15b58-102">SYNOPSIS</span></span>
<span data-ttu-id="15b58-103">Rimuove una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15b58-103">Removes an integration account map.</span></span>

## <span data-ttu-id="15b58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15b58-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b58-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15b58-105">DESCRIPTION</span></span>
<span data-ttu-id="15b58-106">Il cmdlet **Remove-AzIntegrationAccountMap** rimuove una mappa dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15b58-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="15b58-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="15b58-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="15b58-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="15b58-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="15b58-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="15b58-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="15b58-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="15b58-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="15b58-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="15b58-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="15b58-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15b58-112">EXAMPLES</span></span>

### <span data-ttu-id="15b58-113">Esempio 1: rimuovere una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="15b58-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="15b58-114">Questo comando rimuove la mappa dell'account di integrazione denominata IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="15b58-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="15b58-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15b58-115">PARAMETERS</span></span>

### <span data-ttu-id="15b58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b58-116">-DefaultProfile</span></span>
<span data-ttu-id="15b58-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="15b58-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15b58-118">-Force</span><span class="sxs-lookup"><span data-stu-id="15b58-118">-Force</span></span>
<span data-ttu-id="15b58-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="15b58-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15b58-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="15b58-120">-MapName</span></span>
<span data-ttu-id="15b58-121">Specifica il nome della mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15b58-121">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="15b58-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="15b58-122">-Name</span></span>
<span data-ttu-id="15b58-123">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15b58-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="15b58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b58-124">-ResourceGroupName</span></span>
<span data-ttu-id="15b58-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15b58-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="15b58-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15b58-126">-Confirm</span></span>
<span data-ttu-id="15b58-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b58-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b58-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b58-128">-WhatIf</span></span>
<span data-ttu-id="15b58-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15b58-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b58-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15b58-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b58-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b58-131">CommonParameters</span></span>
<span data-ttu-id="15b58-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b58-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b58-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b58-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b58-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15b58-134">INPUTS</span></span>

### <span data-ttu-id="15b58-135">System. String</span><span class="sxs-lookup"><span data-stu-id="15b58-135">System.String</span></span>

## <span data-ttu-id="15b58-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15b58-136">OUTPUTS</span></span>

### <span data-ttu-id="15b58-137">System. void</span><span class="sxs-lookup"><span data-stu-id="15b58-137">System.Void</span></span>

## <span data-ttu-id="15b58-138">Note</span><span class="sxs-lookup"><span data-stu-id="15b58-138">NOTES</span></span>

## <span data-ttu-id="15b58-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15b58-139">RELATED LINKS</span></span>

[<span data-ttu-id="15b58-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="15b58-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="15b58-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="15b58-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="15b58-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="15b58-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


