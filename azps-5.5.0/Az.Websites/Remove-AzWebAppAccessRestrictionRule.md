---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197239"
---
# <span data-ttu-id="f8274-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f8274-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="f8274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8274-102">SYNOPSIS</span></span>
<span data-ttu-id="f8274-103">Rimuove una regola di restrizione di accesso da Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f8274-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="f8274-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8274-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8274-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8274-105">DESCRIPTION</span></span>
<span data-ttu-id="f8274-106">Il cmdlet **Remove-AzWebAppAccessRestrictionRule** rimuove una regola di restrizione di accesso da un'app Web di Azure</span><span class="sxs-lookup"><span data-stu-id="f8274-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="f8274-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8274-107">EXAMPLES</span></span>

### <span data-ttu-id="f8274-108">Esempio 1: Rimuovere una regola di restrizione di accesso all'app Web</span><span class="sxs-lookup"><span data-stu-id="f8274-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="f8274-109">Questo comando rimuove la regola di restrizione di accesso IpRule da Azure Web App denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f8274-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="f8274-110">Esempio 2: Rimuovere una regola di restrizione di accesso all'app Web tag di servizio</span><span class="sxs-lookup"><span data-stu-id="f8274-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="f8274-111">Questo comando rimuove la regola di restrizione di accesso con ServiceTag uguale ad AzureFrontDoor.Backend di Azure Web App denominato ContosoSite che appartiene al gruppo di risorse denominato Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f8274-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f8274-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8274-112">PARAMETERS</span></span>

### <span data-ttu-id="f8274-113">-Action</span><span class="sxs-lookup"><span data-stu-id="f8274-113">-Action</span></span>
<span data-ttu-id="f8274-114">Regola Consenti o Nega.</span><span class="sxs-lookup"><span data-stu-id="f8274-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8274-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8274-115">-DefaultProfile</span></span>
<span data-ttu-id="f8274-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8274-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8274-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f8274-117">-IpAddress</span></span>
<span data-ttu-id="f8274-118">Intervallo IP Address v4 o v6 CIDR.</span><span class="sxs-lookup"><span data-stu-id="f8274-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="f8274-119">Ad esempio: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="f8274-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="f8274-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f8274-120">-Name</span></span>
<span data-ttu-id="f8274-121">Nome regola restrizione di accesso</span><span class="sxs-lookup"><span data-stu-id="f8274-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="f8274-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8274-122">-PassThru</span></span>
<span data-ttu-id="f8274-123">Restituire l'oggetto configurazione della restrizione di accesso.</span><span class="sxs-lookup"><span data-stu-id="f8274-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="f8274-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8274-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8274-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f8274-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8274-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="f8274-126">-ServiceTag</span></span>
<span data-ttu-id="f8274-127">Nome del tag di servizio</span><span class="sxs-lookup"><span data-stu-id="f8274-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="f8274-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="f8274-128">-SlotName</span></span>
<span data-ttu-id="f8274-129">Nome slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f8274-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="f8274-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f8274-130">-SubnetId</span></span>
<span data-ttu-id="f8274-131">ResourceId della subnet.</span><span class="sxs-lookup"><span data-stu-id="f8274-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="f8274-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f8274-132">-SubnetName</span></span>
<span data-ttu-id="f8274-133">Nome subnet.</span><span class="sxs-lookup"><span data-stu-id="f8274-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="f8274-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="f8274-134">-TargetScmSite</span></span>
<span data-ttu-id="f8274-135">La regola è destinata al sito principale o al sito Scm.</span><span class="sxs-lookup"><span data-stu-id="f8274-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="f8274-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f8274-136">-VirtualNetworkName</span></span>
<span data-ttu-id="f8274-137">Nome della rete virtuale (deve essere nello stesso gruppo di risorse di Web App).</span><span class="sxs-lookup"><span data-stu-id="f8274-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="f8274-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f8274-138">-WebAppName</span></span>
<span data-ttu-id="f8274-139">Il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="f8274-139">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8274-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8274-140">-Confirm</span></span>
<span data-ttu-id="f8274-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8274-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8274-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8274-142">-WhatIf</span></span>
<span data-ttu-id="f8274-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8274-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8274-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8274-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8274-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8274-145">CommonParameters</span></span>
<span data-ttu-id="f8274-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8274-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8274-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8274-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8274-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8274-148">INPUTS</span></span>

### <span data-ttu-id="f8274-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f8274-149">System.String</span></span>

## <span data-ttu-id="f8274-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8274-150">OUTPUTS</span></span>

### <span data-ttu-id="f8274-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f8274-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="f8274-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8274-152">NOTES</span></span>

## <span data-ttu-id="f8274-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8274-153">RELATED LINKS</span></span>

[<span data-ttu-id="f8274-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f8274-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="f8274-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f8274-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="f8274-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f8274-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
