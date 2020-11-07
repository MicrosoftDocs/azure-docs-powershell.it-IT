---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864773"
---
# <span data-ttu-id="685a4-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="685a4-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="685a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="685a4-102">SYNOPSIS</span></span>
<span data-ttu-id="685a4-103">Ottiene un blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="685a4-103">Gets a resource lock.</span></span>

## <span data-ttu-id="685a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="685a4-104">SYNTAX</span></span>

### <span data-ttu-id="685a4-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="685a4-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685a4-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="685a4-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="685a4-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="685a4-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685a4-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="685a4-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685a4-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="685a4-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685a4-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="685a4-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="685a4-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="685a4-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="685a4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="685a4-112">DESCRIPTION</span></span>
<span data-ttu-id="685a4-113">Il cmdlet **Get-AzResourceLock** ottiene blocchi di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="685a4-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="685a4-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="685a4-114">EXAMPLES</span></span>

### <span data-ttu-id="685a4-115">Esempio 1: ottenere un blocco</span><span class="sxs-lookup"><span data-stu-id="685a4-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="685a4-116">Questo comando ottiene il blocco delle risorse denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="685a4-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="685a4-117">Esempio 2: ottenere blocchi a livello di gruppo di risorse o superiore</span><span class="sxs-lookup"><span data-stu-id="685a4-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="685a4-118">Questo comando consente di ottenere i blocchi delle risorse nel gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="685a4-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="685a4-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="685a4-119">PARAMETERS</span></span>

### <span data-ttu-id="685a4-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="685a4-120">-ApiVersion</span></span>
<span data-ttu-id="685a4-121">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="685a4-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="685a4-122">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="685a4-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="685a4-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="685a4-123">-AtScope</span></span>
<span data-ttu-id="685a4-124">Indica che questo cmdlet restituisce tutti i blocchi al di sopra dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="685a4-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="685a4-125">Se non specifichi questo parametro, il cmdlet restituirà tutti i blocchi sopra o sotto l'ambito.</span><span class="sxs-lookup"><span data-stu-id="685a4-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="685a4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685a4-126">-DefaultProfile</span></span>
<span data-ttu-id="685a4-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="685a4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="685a4-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="685a4-128">-LockId</span></span>
<span data-ttu-id="685a4-129">Specifica l'ID del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685a4-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="685a4-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="685a4-130">-LockName</span></span>
<span data-ttu-id="685a4-131">Specifica il nome del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685a4-131">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685a4-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="685a4-132">-Pre</span></span>
<span data-ttu-id="685a4-133">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="685a4-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="685a4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="685a4-134">-ResourceGroupName</span></span>
<span data-ttu-id="685a4-135">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="685a4-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="685a4-136">Questo cmdlet ottiene i blocchi per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="685a4-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="685a4-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="685a4-137">-ResourceName</span></span>
<span data-ttu-id="685a4-138">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="685a4-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="685a4-139">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="685a4-139">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685a4-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="685a4-140">-ResourceType</span></span>
<span data-ttu-id="685a4-141">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="685a4-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="685a4-142">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="685a4-142">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685a4-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="685a4-143">-Scope</span></span>
<span data-ttu-id="685a4-144">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="685a4-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="685a4-145">Il cmdlet ottiene i blocchi per questo ambito.</span><span class="sxs-lookup"><span data-stu-id="685a4-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="685a4-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="685a4-146">-TenantLevel</span></span>
<span data-ttu-id="685a4-147">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="685a4-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="685a4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685a4-148">CommonParameters</span></span>
<span data-ttu-id="685a4-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="685a4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685a4-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="685a4-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685a4-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="685a4-151">INPUTS</span></span>

### <span data-ttu-id="685a4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="685a4-152">System.String</span></span>

## <span data-ttu-id="685a4-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="685a4-153">OUTPUTS</span></span>

### <span data-ttu-id="685a4-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="685a4-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="685a4-155">Note</span><span class="sxs-lookup"><span data-stu-id="685a4-155">NOTES</span></span>

## <span data-ttu-id="685a4-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="685a4-156">RELATED LINKS</span></span>

[<span data-ttu-id="685a4-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="685a4-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="685a4-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="685a4-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="685a4-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="685a4-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


