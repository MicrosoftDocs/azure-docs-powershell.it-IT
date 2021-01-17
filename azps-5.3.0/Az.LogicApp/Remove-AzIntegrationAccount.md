---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476153"
---
# <span data-ttu-id="ec84e-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ec84e-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="ec84e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec84e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec84e-103">Rimuove un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ec84e-103">Removes an integration account.</span></span>

## <span data-ttu-id="ec84e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec84e-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec84e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec84e-105">DESCRIPTION</span></span>
<span data-ttu-id="ec84e-106">Il cmdlet **Remove-AzIntegrationAccount** rimuove un account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec84e-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="ec84e-107">Specificare il nome dell'account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec84e-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="ec84e-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="ec84e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ec84e-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="ec84e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ec84e-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="ec84e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ec84e-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="ec84e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ec84e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec84e-112">EXAMPLES</span></span>

### <span data-ttu-id="ec84e-113">Esempio 1: rimuovere un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ec84e-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="ec84e-114">Questo comando rimuove un account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="ec84e-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="ec84e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec84e-115">PARAMETERS</span></span>

### <span data-ttu-id="ec84e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec84e-116">-DefaultProfile</span></span>
<span data-ttu-id="ec84e-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ec84e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec84e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ec84e-118">-Force</span></span>
<span data-ttu-id="ec84e-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ec84e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec84e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec84e-120">-Name</span></span>
<span data-ttu-id="ec84e-121">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ec84e-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="ec84e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec84e-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec84e-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec84e-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ec84e-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec84e-124">-Confirm</span></span>
<span data-ttu-id="ec84e-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec84e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec84e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec84e-126">-WhatIf</span></span>
<span data-ttu-id="ec84e-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec84e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec84e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec84e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec84e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec84e-129">CommonParameters</span></span>
<span data-ttu-id="ec84e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec84e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec84e-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec84e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec84e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec84e-132">INPUTS</span></span>

### <span data-ttu-id="ec84e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ec84e-133">System.String</span></span>

## <span data-ttu-id="ec84e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec84e-134">OUTPUTS</span></span>

### <span data-ttu-id="ec84e-135">System. void</span><span class="sxs-lookup"><span data-stu-id="ec84e-135">System.Void</span></span>

## <span data-ttu-id="ec84e-136">Note</span><span class="sxs-lookup"><span data-stu-id="ec84e-136">NOTES</span></span>

## <span data-ttu-id="ec84e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec84e-137">RELATED LINKS</span></span>

[<span data-ttu-id="ec84e-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ec84e-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="ec84e-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ec84e-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="ec84e-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ec84e-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


