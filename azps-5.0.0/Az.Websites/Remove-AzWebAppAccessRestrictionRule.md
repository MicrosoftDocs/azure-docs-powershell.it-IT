---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202716"
---
# <span data-ttu-id="7babc-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="7babc-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="7babc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7babc-102">SYNOPSIS</span></span>
<span data-ttu-id="7babc-103">Rimuove una regola di restrizione di Access da un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="7babc-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="7babc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7babc-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7babc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7babc-105">DESCRIPTION</span></span>
<span data-ttu-id="7babc-106">Il cmdlet **Remove-AzWebAppAccessRestrictionRule** rimuove una regola di restrizione di Access da un'app Web di Azure</span><span class="sxs-lookup"><span data-stu-id="7babc-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="7babc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7babc-107">EXAMPLES</span></span>

### <span data-ttu-id="7babc-108">Esempio 1: rimuovere una regola di restrizione di Access per l'app Web</span><span class="sxs-lookup"><span data-stu-id="7babc-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="7babc-109">Questo comando rimuove la regola di restrizione di accesso di IpRule da Azure Web App denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="7babc-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7babc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7babc-110">PARAMETERS</span></span>

### <span data-ttu-id="7babc-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="7babc-111">-Action</span></span>
<span data-ttu-id="7babc-112">Consentire o negare la regola.</span><span class="sxs-lookup"><span data-stu-id="7babc-112">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7babc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7babc-113">-DefaultProfile</span></span>
<span data-ttu-id="7babc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7babc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7babc-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="7babc-115">-IpAddress</span></span>
<span data-ttu-id="7babc-116">Indirizzo IP v4 o gamma CIDR V6.</span><span class="sxs-lookup"><span data-stu-id="7babc-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="7babc-117">Ad esempio: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="7babc-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="7babc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7babc-118">-Name</span></span>
<span data-ttu-id="7babc-119">Nome della regola di restrizione di Access</span><span class="sxs-lookup"><span data-stu-id="7babc-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="7babc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7babc-120">-PassThru</span></span>
<span data-ttu-id="7babc-121">Restituisce l'oggetto di configurazione di restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="7babc-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="7babc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7babc-122">-ResourceGroupName</span></span>
<span data-ttu-id="7babc-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7babc-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7babc-124">-Slotname</span><span class="sxs-lookup"><span data-stu-id="7babc-124">-SlotName</span></span>
<span data-ttu-id="7babc-125">Nome dello slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7babc-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="7babc-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7babc-126">-SubnetId</span></span>
<span data-ttu-id="7babc-127">ResourceId della subnet.</span><span class="sxs-lookup"><span data-stu-id="7babc-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="7babc-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7babc-128">-SubnetName</span></span>
<span data-ttu-id="7babc-129">Nome della subnet.</span><span class="sxs-lookup"><span data-stu-id="7babc-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="7babc-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="7babc-130">-TargetScmSite</span></span>
<span data-ttu-id="7babc-131">La regola è destinata al sito principale o all'area SCM.</span><span class="sxs-lookup"><span data-stu-id="7babc-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="7babc-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7babc-132">-VirtualNetworkName</span></span>
<span data-ttu-id="7babc-133">Nome della rete virtuale (deve essere nello stesso gruppo di risorse dell'app Web).</span><span class="sxs-lookup"><span data-stu-id="7babc-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="7babc-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7babc-134">-WebAppName</span></span>
<span data-ttu-id="7babc-135">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="7babc-135">The name of the web app.</span></span>

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

### <span data-ttu-id="7babc-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7babc-136">-Confirm</span></span>
<span data-ttu-id="7babc-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7babc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7babc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7babc-138">-WhatIf</span></span>
<span data-ttu-id="7babc-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7babc-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7babc-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7babc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7babc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7babc-141">CommonParameters</span></span>
<span data-ttu-id="7babc-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7babc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7babc-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7babc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7babc-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7babc-144">INPUTS</span></span>

### <span data-ttu-id="7babc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7babc-145">System.String</span></span>

## <span data-ttu-id="7babc-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7babc-146">OUTPUTS</span></span>

### <span data-ttu-id="7babc-147">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="7babc-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="7babc-148">Note</span><span class="sxs-lookup"><span data-stu-id="7babc-148">NOTES</span></span>

## <span data-ttu-id="7babc-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7babc-149">RELATED LINKS</span></span>

[<span data-ttu-id="7babc-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="7babc-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="7babc-151">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="7babc-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="7babc-152">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="7babc-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
