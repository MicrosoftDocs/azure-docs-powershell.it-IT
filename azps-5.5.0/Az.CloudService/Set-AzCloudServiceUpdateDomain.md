---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4ffb65d4eca9511e179d33c53cb8f515c28aab58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205082"
---
# <span data-ttu-id="f3118-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="f3118-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="f3118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3118-102">SYNOPSIS</span></span>
<span data-ttu-id="f3118-103">Aggiorna le istanze del ruolo nel dominio di aggiornamento specificato.</span><span class="sxs-lookup"><span data-stu-id="f3118-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="f3118-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3118-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f3118-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3118-105">DESCRIPTION</span></span>
<span data-ttu-id="f3118-106">Aggiorna le istanze del ruolo nel dominio di aggiornamento specificato.</span><span class="sxs-lookup"><span data-stu-id="f3118-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="f3118-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3118-107">EXAMPLES</span></span>

### <span data-ttu-id="f3118-108">Esempio 1: Aggiornare l'istanza del ruolo nel dominio di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f3118-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="f3118-109">Questo comando aggiorna le istanze di ruolo nel dominio 0 di aggiornamento del servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="f3118-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="f3118-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3118-110">PARAMETERS</span></span>

### <span data-ttu-id="f3118-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3118-111">-AsJob</span></span>
<span data-ttu-id="f3118-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f3118-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f3118-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f3118-113">-CloudServiceName</span></span>
<span data-ttu-id="f3118-114">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="f3118-114">Name of the cloud service.</span></span>

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

### <span data-ttu-id="f3118-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3118-115">-DefaultProfile</span></span>
<span data-ttu-id="f3118-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3118-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3118-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3118-117">-NoWait</span></span>
<span data-ttu-id="f3118-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f3118-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3118-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3118-119">-PassThru</span></span>
<span data-ttu-id="f3118-120">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="f3118-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3118-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3118-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3118-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3118-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="f3118-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3118-123">-SubscriptionId</span></span>
<span data-ttu-id="f3118-124">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f3118-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f3118-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f3118-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3118-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="f3118-126">-UpdateDomain</span></span>
<span data-ttu-id="f3118-127">Specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f3118-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="f3118-128">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="f3118-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3118-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3118-129">-Confirm</span></span>
<span data-ttu-id="f3118-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3118-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3118-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3118-131">-WhatIf</span></span>
<span data-ttu-id="f3118-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3118-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3118-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3118-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3118-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3118-134">CommonParameters</span></span>
<span data-ttu-id="f3118-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3118-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3118-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3118-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3118-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3118-137">INPUTS</span></span>

## <span data-ttu-id="f3118-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3118-138">OUTPUTS</span></span>

### <span data-ttu-id="f3118-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3118-139">System.Boolean</span></span>

## <span data-ttu-id="f3118-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3118-140">NOTES</span></span>

<span data-ttu-id="f3118-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f3118-141">ALIASES</span></span>

## <span data-ttu-id="f3118-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3118-142">RELATED LINKS</span></span>

