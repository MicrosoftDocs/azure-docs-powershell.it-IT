---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326085"
---
# <span data-ttu-id="b42b4-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b42b4-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="b42b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b42b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b42b4-103">Rimuove una regola di restrizione di Access da un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="b42b4-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="b42b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b42b4-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b42b4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b42b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b42b4-106">Il cmdlet **Remove-AzWebAppAccessRestrictionRule** rimuove una regola di restrizione di Access da un'app Web di Azure</span><span class="sxs-lookup"><span data-stu-id="b42b4-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="b42b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b42b4-107">EXAMPLES</span></span>

### <span data-ttu-id="b42b4-108">Esempio 1: rimuovere una regola di restrizione di Access per l'app Web</span><span class="sxs-lookup"><span data-stu-id="b42b4-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="b42b4-109">Questo comando rimuove la regola di restrizione di accesso di IpRule da Azure Web App denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="b42b4-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="b42b4-110">Esempio 2: rimuovere una regola di restrizione di accesso alle app Web Service Tag</span><span class="sxs-lookup"><span data-stu-id="b42b4-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="b42b4-111">Questo comando rimuove la regola di restrizione di Access con ServiceTag uguale a AzureFrontDoor. backend da Azure Web App denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="b42b4-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b42b4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b42b4-112">PARAMETERS</span></span>

### <span data-ttu-id="b42b4-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="b42b4-113">-Action</span></span>
<span data-ttu-id="b42b4-114">Consentire o negare la regola.</span><span class="sxs-lookup"><span data-stu-id="b42b4-114">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="b42b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b42b4-115">-DefaultProfile</span></span>
<span data-ttu-id="b42b4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b42b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b42b4-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b42b4-117">-IpAddress</span></span>
<span data-ttu-id="b42b4-118">Indirizzo IP v4 o gamma CIDR V6.</span><span class="sxs-lookup"><span data-stu-id="b42b4-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="b42b4-119">Ad esempio: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="b42b4-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="b42b4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b42b4-120">-Name</span></span>
<span data-ttu-id="b42b4-121">Nome della regola di restrizione di Access</span><span class="sxs-lookup"><span data-stu-id="b42b4-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="b42b4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b42b4-122">-PassThru</span></span>
<span data-ttu-id="b42b4-123">Restituisce l'oggetto di configurazione di restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="b42b4-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="b42b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b42b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="b42b4-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b42b4-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b42b4-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="b42b4-126">-ServiceTag</span></span>
<span data-ttu-id="b42b4-127">Nome del tag servizio</span><span class="sxs-lookup"><span data-stu-id="b42b4-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="b42b4-128">-Slotname</span><span class="sxs-lookup"><span data-stu-id="b42b4-128">-SlotName</span></span>
<span data-ttu-id="b42b4-129">Nome dello slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b42b4-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="b42b4-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b42b4-130">-SubnetId</span></span>
<span data-ttu-id="b42b4-131">ResourceId della subnet.</span><span class="sxs-lookup"><span data-stu-id="b42b4-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="b42b4-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b42b4-132">-SubnetName</span></span>
<span data-ttu-id="b42b4-133">Nome della subnet.</span><span class="sxs-lookup"><span data-stu-id="b42b4-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="b42b4-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="b42b4-134">-TargetScmSite</span></span>
<span data-ttu-id="b42b4-135">La regola è destinata al sito principale o all'area SCM.</span><span class="sxs-lookup"><span data-stu-id="b42b4-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="b42b4-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b42b4-136">-VirtualNetworkName</span></span>
<span data-ttu-id="b42b4-137">Nome della rete virtuale (deve essere nello stesso gruppo di risorse dell'app Web).</span><span class="sxs-lookup"><span data-stu-id="b42b4-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="b42b4-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b42b4-138">-WebAppName</span></span>
<span data-ttu-id="b42b4-139">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="b42b4-139">The name of the web app.</span></span>

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

### <span data-ttu-id="b42b4-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b42b4-140">-Confirm</span></span>
<span data-ttu-id="b42b4-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b42b4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b42b4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b42b4-142">-WhatIf</span></span>
<span data-ttu-id="b42b4-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b42b4-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b42b4-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b42b4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b42b4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b42b4-145">CommonParameters</span></span>
<span data-ttu-id="b42b4-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b42b4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b42b4-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b42b4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b42b4-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b42b4-148">INPUTS</span></span>

### <span data-ttu-id="b42b4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b42b4-149">System.String</span></span>

## <span data-ttu-id="b42b4-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b42b4-150">OUTPUTS</span></span>

### <span data-ttu-id="b42b4-151">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b42b4-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="b42b4-152">Note</span><span class="sxs-lookup"><span data-stu-id="b42b4-152">NOTES</span></span>

## <span data-ttu-id="b42b4-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b42b4-153">RELATED LINKS</span></span>

[<span data-ttu-id="b42b4-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b42b4-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="b42b4-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="b42b4-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="b42b4-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="b42b4-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
