---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519537"
---
# <span data-ttu-id="7f382-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f382-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="7f382-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f382-102">SYNOPSIS</span></span>
<span data-ttu-id="7f382-103">Ottiene un blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7f382-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f382-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f382-104">SYNTAX</span></span>

### <span data-ttu-id="7f382-105">Un blocco nell'ambito del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7f382-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f382-106">Un blocco nell'ambito delle risorse del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7f382-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f382-107">Un blocco nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="7f382-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f382-108">Un blocco nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7f382-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f382-109">Un blocco nell'ambito delle risorse dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7f382-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f382-110">Un blocco nell'ambito delle risorse del tenant.</span><span class="sxs-lookup"><span data-stu-id="7f382-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f382-111">Un blocco, per ID.</span><span class="sxs-lookup"><span data-stu-id="7f382-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f382-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f382-112">DESCRIPTION</span></span>
<span data-ttu-id="7f382-113">Il cmdlet **Get-AzureRmResourceLock** ottiene blocchi di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="7f382-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="7f382-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f382-114">EXAMPLES</span></span>

### <span data-ttu-id="7f382-115">Esempio 1: ottenere un blocco</span><span class="sxs-lookup"><span data-stu-id="7f382-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7f382-116">Questo comando ottiene il blocco delle risorse denominato ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="7f382-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="7f382-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f382-117">PARAMETERS</span></span>

### <span data-ttu-id="7f382-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7f382-118">-ApiVersion</span></span>
<span data-ttu-id="7f382-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7f382-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7f382-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f382-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7f382-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="7f382-121">-AtScope</span></span>
<span data-ttu-id="7f382-122">Indica che questo cmdlet restituisce tutti i blocchi al di sopra dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="7f382-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="7f382-123">Se non specifichi questo parametro, il cmdlet restituirà tutti i blocchi sopra o sotto l'ambito.</span><span class="sxs-lookup"><span data-stu-id="7f382-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="7f382-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7f382-124">-InformationAction</span></span>
<span data-ttu-id="7f382-125">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7f382-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7f382-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f382-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f382-127">Continuare</span><span class="sxs-lookup"><span data-stu-id="7f382-127">Continue</span></span>
- <span data-ttu-id="7f382-128">Ignora</span><span class="sxs-lookup"><span data-stu-id="7f382-128">Ignore</span></span>
- <span data-ttu-id="7f382-129">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7f382-129">Inquire</span></span>
- <span data-ttu-id="7f382-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7f382-130">SilentlyContinue</span></span>
- <span data-ttu-id="7f382-131">Stop</span><span class="sxs-lookup"><span data-stu-id="7f382-131">Stop</span></span>
- <span data-ttu-id="7f382-132">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7f382-132">Suspend</span></span>

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

### <span data-ttu-id="7f382-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7f382-133">-InformationVariable</span></span>
<span data-ttu-id="7f382-134">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f382-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7f382-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="7f382-135">-LockId</span></span>
<span data-ttu-id="7f382-136">Specifica l'ID del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f382-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-137">-LockName</span><span class="sxs-lookup"><span data-stu-id="7f382-137">-LockName</span></span>
<span data-ttu-id="7f382-138">Specifica il nome del blocco ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f382-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="7f382-139">-Pre</span></span>
<span data-ttu-id="7f382-140">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7f382-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7f382-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f382-141">-ResourceGroupName</span></span>
<span data-ttu-id="7f382-142">Specifica il nome del gruppo di risorse per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f382-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="7f382-143">Questo cmdlet ottiene i blocchi per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7f382-143">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7f382-144">-ResourceName</span></span>
<span data-ttu-id="7f382-145">Specifica il nome della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f382-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="7f382-146">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7f382-146">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7f382-147">-ResourceType</span></span>
<span data-ttu-id="7f382-148">Specifica il tipo di risorsa della risorsa per cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f382-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="7f382-149">Questo cmdlet ottiene i blocchi per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7f382-149">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-150">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7f382-150">-Scope</span></span>
<span data-ttu-id="7f382-151">Specifica l'ambito a cui si applica il blocco.</span><span class="sxs-lookup"><span data-stu-id="7f382-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="7f382-152">Il cmdlet ottiene i blocchi per questo ambito.</span><span class="sxs-lookup"><span data-stu-id="7f382-152">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7f382-153">-TenantLevel</span></span>
<span data-ttu-id="7f382-154">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="7f382-154">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f382-155">-DefaultProfile</span></span>
<span data-ttu-id="7f382-156">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f382-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f382-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f382-157">CommonParameters</span></span>
<span data-ttu-id="7f382-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f382-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f382-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f382-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f382-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f382-160">INPUTS</span></span>

## <span data-ttu-id="7f382-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f382-161">OUTPUTS</span></span>

### <span data-ttu-id="7f382-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7f382-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7f382-163">Note</span><span class="sxs-lookup"><span data-stu-id="7f382-163">NOTES</span></span>

## <span data-ttu-id="7f382-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f382-164">RELATED LINKS</span></span>

[<span data-ttu-id="7f382-165">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f382-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="7f382-166">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f382-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="7f382-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="7f382-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


