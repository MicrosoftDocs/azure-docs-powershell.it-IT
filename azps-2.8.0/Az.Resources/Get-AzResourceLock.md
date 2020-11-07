---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856425"
---
# <span data-ttu-id="3ca04-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3ca04-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="3ca04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ca04-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca04-103">Ottiene un blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="3ca04-103">Gets a resource lock.</span></span>

## <span data-ttu-id="3ca04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ca04-104">SYNTAX</span></span>

### <span data-ttu-id="3ca04-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ca04-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca04-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="3ca04-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ca04-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="3ca04-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca04-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="3ca04-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca04-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="3ca04-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca04-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="3ca04-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca04-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="3ca04-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ca04-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ca04-112">DESCRIPTION</span></span>
<span data-ttu-id="3ca04-113">Il cmdlet **Get-AzResourceLock** ottiene blocchi di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca04-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="3ca04-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ca04-114">EXAMPLES</span></span>

### <span data-ttu-id="3ca04-115">Esempio 1: ottenere un blocco</span><span class="sxs-lookup"><span data-stu-id="3ca04-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3ca04-116">Questo comando ottiene il blocco delle risorse denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="3ca04-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="3ca04-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ca04-117">PARAMETERS</span></span>

### <span data-ttu-id="3ca04-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3ca04-118">-ApiVersion</span></span>
<span data-ttu-id="3ca04-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="3ca04-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3ca04-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="3ca04-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3ca04-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="3ca04-121">-AtScope</span></span>
<span data-ttu-id="3ca04-122">Indica che questo cmdlet restituisce tutti i blocchi al di sopra dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="3ca04-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="3ca04-123">Se non specifichi questo parametro, il cmdlet restituirà tutti i blocchi sopra o sotto l'ambito.</span><span class="sxs-lookup"><span data-stu-id="3ca04-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="3ca04-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca04-124">-DefaultProfile</span></span>
<span data-ttu-id="3ca04-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ca04-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ca04-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="3ca04-126">-LockId</span></span>
<span data-ttu-id="3ca04-127">Specifica l'ID del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca04-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3ca04-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="3ca04-128">-LockName</span></span>
<span data-ttu-id="3ca04-129">Specifica il nome del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca04-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3ca04-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="3ca04-130">-Pre</span></span>
<span data-ttu-id="3ca04-131">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3ca04-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3ca04-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca04-132">-ResourceGroupName</span></span>
<span data-ttu-id="3ca04-133">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="3ca04-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="3ca04-134">Questo cmdlet ottiene i blocchi per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ca04-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="3ca04-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3ca04-135">-ResourceName</span></span>
<span data-ttu-id="3ca04-136">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="3ca04-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="3ca04-137">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3ca04-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="3ca04-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3ca04-138">-ResourceType</span></span>
<span data-ttu-id="3ca04-139">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="3ca04-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="3ca04-140">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3ca04-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="3ca04-141">-Ambito</span><span class="sxs-lookup"><span data-stu-id="3ca04-141">-Scope</span></span>
<span data-ttu-id="3ca04-142">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="3ca04-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="3ca04-143">Il cmdlet ottiene i blocchi per questo ambito.</span><span class="sxs-lookup"><span data-stu-id="3ca04-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="3ca04-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3ca04-144">-TenantLevel</span></span>
<span data-ttu-id="3ca04-145">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="3ca04-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="3ca04-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca04-146">CommonParameters</span></span>
<span data-ttu-id="3ca04-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca04-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca04-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca04-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca04-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ca04-149">INPUTS</span></span>

### <span data-ttu-id="3ca04-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca04-150">System.String</span></span>

## <span data-ttu-id="3ca04-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ca04-151">OUTPUTS</span></span>

### <span data-ttu-id="3ca04-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3ca04-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3ca04-153">Note</span><span class="sxs-lookup"><span data-stu-id="3ca04-153">NOTES</span></span>

## <span data-ttu-id="3ca04-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ca04-154">RELATED LINKS</span></span>

[<span data-ttu-id="3ca04-155">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3ca04-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="3ca04-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3ca04-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="3ca04-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="3ca04-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


