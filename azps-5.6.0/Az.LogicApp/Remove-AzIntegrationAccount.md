---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: d1f15544223a20113a40975780aa8ca899205f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961998"
---
# <span data-ttu-id="3bc7a-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3bc7a-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="3bc7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bc7a-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc7a-103">Rimuove un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-103">Removes an integration account.</span></span>

## <span data-ttu-id="3bc7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bc7a-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc7a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3bc7a-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc7a-106">Il cmdlet **Remove-AzIntegrationAccount** rimuove un account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="3bc7a-107">Specificare il nome dell'account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="3bc7a-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3bc7a-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3bc7a-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3bc7a-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3bc7a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bc7a-112">EXAMPLES</span></span>

### <span data-ttu-id="3bc7a-113">Esempio 1: Rimuovere un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="3bc7a-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="3bc7a-114">Questo comando rimuove un account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="3bc7a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bc7a-115">PARAMETERS</span></span>

### <span data-ttu-id="3bc7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc7a-116">-DefaultProfile</span></span>
<span data-ttu-id="3bc7a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3bc7a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bc7a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3bc7a-118">-Force</span></span>
<span data-ttu-id="3bc7a-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3bc7a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3bc7a-120">-Name</span></span>
<span data-ttu-id="3bc7a-121">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="3bc7a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc7a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3bc7a-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3bc7a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bc7a-124">-Confirm</span></span>
<span data-ttu-id="3bc7a-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc7a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc7a-126">-WhatIf</span></span>
<span data-ttu-id="3bc7a-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc7a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc7a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc7a-129">CommonParameters</span></span>
<span data-ttu-id="3bc7a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc7a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc7a-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc7a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc7a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="3bc7a-132">INPUTS</span></span>

### <span data-ttu-id="3bc7a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3bc7a-133">System.String</span></span>

## <span data-ttu-id="3bc7a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bc7a-134">OUTPUTS</span></span>

### <span data-ttu-id="3bc7a-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="3bc7a-135">System.Void</span></span>

## <span data-ttu-id="3bc7a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="3bc7a-136">NOTES</span></span>

## <span data-ttu-id="3bc7a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bc7a-137">RELATED LINKS</span></span>

[<span data-ttu-id="3bc7a-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3bc7a-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="3bc7a-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3bc7a-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="3bc7a-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3bc7a-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


