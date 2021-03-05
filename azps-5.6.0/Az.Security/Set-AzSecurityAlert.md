---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 889e4a0651c9aa3ccbe91227db803958fcb3c7bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986577"
---
# <span data-ttu-id="408bd-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="408bd-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="408bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408bd-102">SYNOPSIS</span></span>
<span data-ttu-id="408bd-103">Aggiorna lo stato di un avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="408bd-103">Updates a security alert state.</span></span>

## <span data-ttu-id="408bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="408bd-104">SYNTAX</span></span>

### <span data-ttu-id="408bd-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="408bd-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="408bd-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="408bd-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="408bd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="408bd-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="408bd-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="408bd-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="408bd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="408bd-109">DESCRIPTION</span></span>
<span data-ttu-id="408bd-110">Imposta lo stato di un avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="408bd-110">Sets a security alert state.</span></span>

## <span data-ttu-id="408bd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="408bd-111">EXAMPLES</span></span>

### <span data-ttu-id="408bd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="408bd-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="408bd-113">Ignora un avviso di sicurezza elevato.</span><span class="sxs-lookup"><span data-stu-id="408bd-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="408bd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="408bd-114">PARAMETERS</span></span>

### <span data-ttu-id="408bd-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="408bd-115">-ActionType</span></span>
<span data-ttu-id="408bd-116">Tipo di azione.</span><span class="sxs-lookup"><span data-stu-id="408bd-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408bd-117">-DefaultProfile</span></span>
<span data-ttu-id="408bd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="408bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="408bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="408bd-119">-InputObject</span></span>
<span data-ttu-id="408bd-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="408bd-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-121">-Location</span><span class="sxs-lookup"><span data-stu-id="408bd-121">-Location</span></span>
<span data-ttu-id="408bd-122">Posizione.</span><span class="sxs-lookup"><span data-stu-id="408bd-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="408bd-123">-Name</span></span>
<span data-ttu-id="408bd-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="408bd-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="408bd-125">-PassThru</span></span>
<span data-ttu-id="408bd-126">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="408bd-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="408bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="408bd-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="408bd-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="408bd-129">-ResourceId</span></span>
<span data-ttu-id="408bd-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="408bd-130">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="408bd-131">-Confirm</span></span>
<span data-ttu-id="408bd-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="408bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408bd-133">-WhatIf</span></span>
<span data-ttu-id="408bd-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="408bd-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="408bd-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="408bd-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408bd-136">CommonParameters</span></span>
<span data-ttu-id="408bd-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408bd-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="408bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408bd-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="408bd-139">INPUTS</span></span>

### <span data-ttu-id="408bd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="408bd-140">System.String</span></span>

### <span data-ttu-id="408bd-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="408bd-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="408bd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="408bd-142">OUTPUTS</span></span>

### <span data-ttu-id="408bd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="408bd-143">System.Boolean</span></span>

## <span data-ttu-id="408bd-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="408bd-144">NOTES</span></span>

## <span data-ttu-id="408bd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="408bd-145">RELATED LINKS</span></span>
