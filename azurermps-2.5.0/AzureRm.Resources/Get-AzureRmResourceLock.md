---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866429"
---
# <span data-ttu-id="60ce5-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60ce5-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="60ce5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="60ce5-103">Ottiene un blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="60ce5-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ce5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60ce5-104">SYNTAX</span></span>

### <span data-ttu-id="60ce5-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60ce5-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60ce5-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="60ce5-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60ce5-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="60ce5-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60ce5-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="60ce5-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60ce5-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="60ce5-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60ce5-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="60ce5-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="60ce5-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="60ce5-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="60ce5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60ce5-112">DESCRIPTION</span></span>
<span data-ttu-id="60ce5-113">Il cmdlet **Get-AzureRmResourceLock** ottiene blocchi di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="60ce5-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="60ce5-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60ce5-114">EXAMPLES</span></span>

### <span data-ttu-id="60ce5-115">Esempio 1: ottenere un blocco</span><span class="sxs-lookup"><span data-stu-id="60ce5-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="60ce5-116">Questo comando ottiene il blocco delle risorse denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="60ce5-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="60ce5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60ce5-117">PARAMETERS</span></span>

### <span data-ttu-id="60ce5-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="60ce5-118">-ApiVersion</span></span>
<span data-ttu-id="60ce5-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="60ce5-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="60ce5-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="60ce5-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="60ce5-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="60ce5-121">-AtScope</span></span>
<span data-ttu-id="60ce5-122">Indica che questo cmdlet restituisce tutti i blocchi al di sopra dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="60ce5-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="60ce5-123">Se non specifichi questo parametro, il cmdlet restituirà tutti i blocchi sopra o sotto l'ambito.</span><span class="sxs-lookup"><span data-stu-id="60ce5-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="60ce5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ce5-124">-DefaultProfile</span></span>
<span data-ttu-id="60ce5-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="60ce5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ce5-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="60ce5-126">-InformationAction</span></span>
<span data-ttu-id="60ce5-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="60ce5-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="60ce5-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="60ce5-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="60ce5-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="60ce5-129">Continue</span></span>
- <span data-ttu-id="60ce5-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="60ce5-130">Ignore</span></span>
- <span data-ttu-id="60ce5-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="60ce5-131">Inquire</span></span>
- <span data-ttu-id="60ce5-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="60ce5-132">SilentlyContinue</span></span>
- <span data-ttu-id="60ce5-133">Stop</span><span class="sxs-lookup"><span data-stu-id="60ce5-133">Stop</span></span>
- <span data-ttu-id="60ce5-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="60ce5-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ce5-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="60ce5-135">-InformationVariable</span></span>
<span data-ttu-id="60ce5-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="60ce5-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ce5-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="60ce5-137">-LockId</span></span>
<span data-ttu-id="60ce5-138">Specifica l'ID del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60ce5-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="60ce5-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="60ce5-139">-LockName</span></span>
<span data-ttu-id="60ce5-140">Specifica il nome del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60ce5-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="60ce5-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="60ce5-141">-Pre</span></span>
<span data-ttu-id="60ce5-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="60ce5-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="60ce5-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ce5-143">-ResourceGroupName</span></span>
<span data-ttu-id="60ce5-144">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="60ce5-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="60ce5-145">Questo cmdlet ottiene i blocchi per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60ce5-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="60ce5-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="60ce5-146">-ResourceName</span></span>
<span data-ttu-id="60ce5-147">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="60ce5-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="60ce5-148">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="60ce5-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="60ce5-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="60ce5-149">-ResourceType</span></span>
<span data-ttu-id="60ce5-150">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="60ce5-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="60ce5-151">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="60ce5-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="60ce5-152">-Ambito</span><span class="sxs-lookup"><span data-stu-id="60ce5-152">-Scope</span></span>
<span data-ttu-id="60ce5-153">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="60ce5-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="60ce5-154">Il cmdlet ottiene i blocchi per questo ambito.</span><span class="sxs-lookup"><span data-stu-id="60ce5-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="60ce5-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="60ce5-155">-TenantLevel</span></span>
<span data-ttu-id="60ce5-156">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="60ce5-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="60ce5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ce5-157">CommonParameters</span></span>
<span data-ttu-id="60ce5-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60ce5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ce5-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ce5-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ce5-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60ce5-160">INPUTS</span></span>

## <span data-ttu-id="60ce5-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60ce5-161">OUTPUTS</span></span>

## <span data-ttu-id="60ce5-162">Note</span><span class="sxs-lookup"><span data-stu-id="60ce5-162">NOTES</span></span>

## <span data-ttu-id="60ce5-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60ce5-163">RELATED LINKS</span></span>

[<span data-ttu-id="60ce5-164">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60ce5-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="60ce5-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60ce5-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="60ce5-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60ce5-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


