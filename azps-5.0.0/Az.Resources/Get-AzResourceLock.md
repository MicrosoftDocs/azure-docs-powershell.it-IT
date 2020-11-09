---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301099"
---
# <span data-ttu-id="c2d13-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c2d13-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="c2d13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2d13-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d13-103">Ottiene un blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c2d13-103">Gets a resource lock.</span></span>

## <span data-ttu-id="c2d13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2d13-104">SYNTAX</span></span>

### <span data-ttu-id="c2d13-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c2d13-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d13-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c2d13-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d13-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="c2d13-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d13-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c2d13-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d13-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c2d13-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d13-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="c2d13-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2d13-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2d13-111">DESCRIPTION</span></span>
<span data-ttu-id="c2d13-112">Il cmdlet **Get-AzResourceLock** ottiene blocchi di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d13-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="c2d13-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2d13-113">EXAMPLES</span></span>

### <span data-ttu-id="c2d13-114">Esempio 1: ottenere un blocco</span><span class="sxs-lookup"><span data-stu-id="c2d13-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c2d13-115">Questo comando ottiene il blocco delle risorse denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="c2d13-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="c2d13-116">Esempio 2: ottenere blocchi a livello di gruppo di risorse o superiore</span><span class="sxs-lookup"><span data-stu-id="c2d13-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="c2d13-117">Questo comando consente di ottenere i blocchi delle risorse nel gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c2d13-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="c2d13-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2d13-118">PARAMETERS</span></span>

### <span data-ttu-id="c2d13-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c2d13-119">-ApiVersion</span></span>
<span data-ttu-id="c2d13-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="c2d13-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c2d13-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2d13-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2d13-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="c2d13-122">-AtScope</span></span>
<span data-ttu-id="c2d13-123">Indica che questo cmdlet restituisce tutti i blocchi al di sopra dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="c2d13-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="c2d13-124">Se non specifichi questo parametro, il cmdlet restituirà tutti i blocchi sopra o sotto l'ambito.</span><span class="sxs-lookup"><span data-stu-id="c2d13-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="c2d13-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d13-125">-DefaultProfile</span></span>
<span data-ttu-id="c2d13-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c2d13-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2d13-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="c2d13-127">-LockId</span></span>
<span data-ttu-id="c2d13-128">Specifica l'ID del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2d13-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d13-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="c2d13-129">-LockName</span></span>
<span data-ttu-id="c2d13-130">Specifica il nome del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2d13-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d13-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="c2d13-131">-Pre</span></span>
<span data-ttu-id="c2d13-132">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c2d13-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c2d13-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d13-133">-ResourceGroupName</span></span>
<span data-ttu-id="c2d13-134">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="c2d13-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="c2d13-135">Questo cmdlet ottiene i blocchi per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2d13-135">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d13-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c2d13-136">-ResourceName</span></span>
<span data-ttu-id="c2d13-137">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="c2d13-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="c2d13-138">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2d13-138">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d13-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c2d13-139">-ResourceType</span></span>
<span data-ttu-id="c2d13-140">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="c2d13-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="c2d13-141">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2d13-141">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d13-142">-Ambito</span><span class="sxs-lookup"><span data-stu-id="c2d13-142">-Scope</span></span>
<span data-ttu-id="c2d13-143">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="c2d13-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c2d13-144">Il cmdlet ottiene i blocchi per questo ambito.</span><span class="sxs-lookup"><span data-stu-id="c2d13-144">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d13-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d13-145">CommonParameters</span></span>
<span data-ttu-id="c2d13-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2d13-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d13-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2d13-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d13-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2d13-148">INPUTS</span></span>

### <span data-ttu-id="c2d13-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c2d13-149">System.String</span></span>

## <span data-ttu-id="c2d13-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2d13-150">OUTPUTS</span></span>

### <span data-ttu-id="c2d13-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c2d13-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c2d13-152">Note</span><span class="sxs-lookup"><span data-stu-id="c2d13-152">NOTES</span></span>

## <span data-ttu-id="c2d13-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2d13-153">RELATED LINKS</span></span>

[<span data-ttu-id="c2d13-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c2d13-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="c2d13-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c2d13-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="c2d13-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c2d13-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


