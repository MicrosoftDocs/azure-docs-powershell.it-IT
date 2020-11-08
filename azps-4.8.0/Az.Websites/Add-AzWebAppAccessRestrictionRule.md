---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190413"
---
# <span data-ttu-id="cd2fa-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="cd2fa-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="cd2fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2fa-103">Aggiunge una regola di restiction di Access a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="cd2fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd2fa-104">SYNTAX</span></span>

### <span data-ttu-id="cd2fa-105">IpAddressParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd2fa-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd2fa-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd2fa-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd2fa-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd2fa-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd2fa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd2fa-108">DESCRIPTION</span></span>
<span data-ttu-id="cd2fa-109">Il cmdlet **Add-AzWebAppAccessRestrictionRule** aggiunge una regola di restrizione di Access a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="cd2fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd2fa-110">EXAMPLES</span></span>

### <span data-ttu-id="cd2fa-111">Esempio 1: aggiungere la regola di restrizione dell'accesso IpAddress a un'app Web</span><span class="sxs-lookup"><span data-stu-id="cd2fa-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="cd2fa-112">Questo comando aggiunge una regola di restrizione di Access con priorità 200 e un intervallo IP a un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="cd2fa-113">Esempio 2: aggiungere la regola di restrizione di accesso al servizio subnet in un'app Web</span><span class="sxs-lookup"><span data-stu-id="cd2fa-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="cd2fa-114">Questo comando aggiunge una regola di restrizione di Access con priorità 300 e subnet appgw-subnet in Corp-VNET a un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="cd2fa-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd2fa-115">PARAMETERS</span></span>

### <span data-ttu-id="cd2fa-116">-Azione</span><span class="sxs-lookup"><span data-stu-id="cd2fa-116">-Action</span></span>
<span data-ttu-id="cd2fa-117">Consentire o negare la regola.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-117">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="cd2fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2fa-118">-DefaultProfile</span></span>
<span data-ttu-id="cd2fa-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd2fa-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd2fa-120">-Description</span></span>
<span data-ttu-id="cd2fa-121">Descrizione della restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="cd2fa-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd2fa-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="cd2fa-123">Specificare se la registrazione dell'endpoint del servizio nella subnet deve essere convalidata.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2fa-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="cd2fa-124">-IpAddress</span></span>
<span data-ttu-id="cd2fa-125">Indirizzo IP v4 o gamma CIDR V6.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="cd2fa-126">Ad esempio: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="cd2fa-126">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2fa-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd2fa-127">-Name</span></span>
<span data-ttu-id="cd2fa-128">Nome regola</span><span class="sxs-lookup"><span data-stu-id="cd2fa-128">Rule Name</span></span>

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

### <span data-ttu-id="cd2fa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd2fa-129">-PassThru</span></span>
<span data-ttu-id="cd2fa-130">Restituisce l'oggetto di configurazione di restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="cd2fa-131">-Priorità</span><span class="sxs-lookup"><span data-stu-id="cd2fa-131">-Priority</span></span>
<span data-ttu-id="cd2fa-132">Priorità restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-132">Access Restriction priority.</span></span> <span data-ttu-id="cd2fa-133">Ad esempio: 500.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-133">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2fa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd2fa-134">-ResourceGroupName</span></span>
<span data-ttu-id="cd2fa-135">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cd2fa-135">Resource Group Name</span></span>

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

### <span data-ttu-id="cd2fa-136">-Slotname</span><span class="sxs-lookup"><span data-stu-id="cd2fa-136">-SlotName</span></span>
<span data-ttu-id="cd2fa-137">Nome dello slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="cd2fa-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cd2fa-138">-SubnetId</span></span>
<span data-ttu-id="cd2fa-139">ResourceId della subnet.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-139">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2fa-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cd2fa-140">-SubnetName</span></span>
<span data-ttu-id="cd2fa-141">Nome della subnet.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-141">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2fa-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="cd2fa-142">-TargetScmSite</span></span>
<span data-ttu-id="cd2fa-143">La regola è destinata al sito principale o all'area SCM.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="cd2fa-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cd2fa-144">-VirtualNetworkName</span></span>
<span data-ttu-id="cd2fa-145">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-145">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd2fa-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="cd2fa-146">-WebAppName</span></span>
<span data-ttu-id="cd2fa-147">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-147">The name of the web app.</span></span>

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

### <span data-ttu-id="cd2fa-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd2fa-148">-Confirm</span></span>
<span data-ttu-id="cd2fa-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd2fa-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2fa-150">-WhatIf</span></span>
<span data-ttu-id="cd2fa-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd2fa-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd2fa-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2fa-153">CommonParameters</span></span>
<span data-ttu-id="cd2fa-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2fa-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd2fa-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2fa-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd2fa-156">INPUTS</span></span>

### <span data-ttu-id="cd2fa-157">System. String</span><span class="sxs-lookup"><span data-stu-id="cd2fa-157">System.String</span></span>

## <span data-ttu-id="cd2fa-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd2fa-158">OUTPUTS</span></span>

### <span data-ttu-id="cd2fa-159">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="cd2fa-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="cd2fa-160">Note</span><span class="sxs-lookup"><span data-stu-id="cd2fa-160">NOTES</span></span>

## <span data-ttu-id="cd2fa-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd2fa-161">RELATED LINKS</span></span>

[<span data-ttu-id="cd2fa-162">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="cd2fa-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="cd2fa-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="cd2fa-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="cd2fa-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="cd2fa-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
