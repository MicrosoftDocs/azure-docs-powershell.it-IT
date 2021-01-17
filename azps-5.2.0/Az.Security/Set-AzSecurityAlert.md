---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335431"
---
# <span data-ttu-id="14fc2-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="14fc2-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="14fc2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="14fc2-103">Aggiorna uno stato di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="14fc2-103">Updates a security alert state.</span></span>

## <span data-ttu-id="14fc2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14fc2-104">SYNTAX</span></span>

### <span data-ttu-id="14fc2-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14fc2-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14fc2-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="14fc2-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14fc2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14fc2-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14fc2-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="14fc2-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14fc2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14fc2-109">DESCRIPTION</span></span>
<span data-ttu-id="14fc2-110">Imposta uno stato di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="14fc2-110">Sets a security alert state.</span></span>

## <span data-ttu-id="14fc2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14fc2-111">EXAMPLES</span></span>

### <span data-ttu-id="14fc2-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14fc2-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="14fc2-113">Respinge un avviso di sicurezza generato.</span><span class="sxs-lookup"><span data-stu-id="14fc2-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="14fc2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14fc2-114">PARAMETERS</span></span>

### <span data-ttu-id="14fc2-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="14fc2-115">-ActionType</span></span>
<span data-ttu-id="14fc2-116">Tipo di azione.</span><span class="sxs-lookup"><span data-stu-id="14fc2-116">Action Type.</span></span>

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

### <span data-ttu-id="14fc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14fc2-117">-DefaultProfile</span></span>
<span data-ttu-id="14fc2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14fc2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14fc2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14fc2-119">-InputObject</span></span>
<span data-ttu-id="14fc2-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="14fc2-120">Input Object.</span></span>

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

### <span data-ttu-id="14fc2-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="14fc2-121">-Location</span></span>
<span data-ttu-id="14fc2-122">Posizione.</span><span class="sxs-lookup"><span data-stu-id="14fc2-122">Location.</span></span>

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

### <span data-ttu-id="14fc2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="14fc2-123">-Name</span></span>
<span data-ttu-id="14fc2-124">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="14fc2-124">Resource name.</span></span>

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

### <span data-ttu-id="14fc2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14fc2-125">-PassThru</span></span>
<span data-ttu-id="14fc2-126">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="14fc2-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="14fc2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14fc2-127">-ResourceGroupName</span></span>
<span data-ttu-id="14fc2-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14fc2-128">Resource group name.</span></span>

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

### <span data-ttu-id="14fc2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14fc2-129">-ResourceId</span></span>
<span data-ttu-id="14fc2-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="14fc2-130">Resource ID.</span></span>

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

### <span data-ttu-id="14fc2-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14fc2-131">-Confirm</span></span>
<span data-ttu-id="14fc2-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14fc2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14fc2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14fc2-133">-WhatIf</span></span>
<span data-ttu-id="14fc2-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14fc2-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14fc2-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14fc2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14fc2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fc2-136">CommonParameters</span></span>
<span data-ttu-id="14fc2-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14fc2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fc2-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14fc2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fc2-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14fc2-139">INPUTS</span></span>

### <span data-ttu-id="14fc2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="14fc2-140">System.String</span></span>

### <span data-ttu-id="14fc2-141">Microsoft. Azure. Commands. Security. Models. alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="14fc2-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="14fc2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14fc2-142">OUTPUTS</span></span>

### <span data-ttu-id="14fc2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14fc2-143">System.Boolean</span></span>

## <span data-ttu-id="14fc2-144">Note</span><span class="sxs-lookup"><span data-stu-id="14fc2-144">NOTES</span></span>

## <span data-ttu-id="14fc2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14fc2-145">RELATED LINKS</span></span>
