---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188719"
---
# <span data-ttu-id="4fa1f-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4fa1f-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="4fa1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fa1f-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa1f-103">Aggiunge una regola di ritienizione di Access a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="4fa1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fa1f-104">SYNTAX</span></span>

### <span data-ttu-id="4fa1f-105">IpAddressParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4fa1f-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fa1f-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fa1f-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fa1f-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fa1f-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fa1f-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fa1f-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa1f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4fa1f-109">DESCRIPTION</span></span>
<span data-ttu-id="4fa1f-110">Il cmdlet **Add-AzWebAppAccessRestrictionRule** aggiunge una regola di restrizione di accesso a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="4fa1f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fa1f-111">EXAMPLES</span></span>

### <span data-ttu-id="4fa1f-112">Esempio 1: Aggiungere una regola di restrizione di accesso IpAddress a un'app Web</span><span class="sxs-lookup"><span data-stu-id="4fa1f-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="4fa1f-113">Questo comando aggiunge una regola di restrizione di accesso con priorità 200 e un intervallo IP a un'app Web denominata ContosoSite che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="4fa1f-114">Esempio 2: Aggiungere la regola di restrizione di accesso all'endpoint del servizio subnet a un'app Web</span><span class="sxs-lookup"><span data-stu-id="4fa1f-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="4fa1f-115">Questo comando aggiunge una regola di restrizione di accesso con priorità 300 e con subnet appgw-subnet in corp-vnet a un'app Web denominata ContosoSite che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="4fa1f-116">Esempio 3: Aggiungere una regola di restrizione di accesso ServiceTag a un'app Web</span><span class="sxs-lookup"><span data-stu-id="4fa1f-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="4fa1f-117">Questo comando aggiunge una regola di restrizione di accesso con priorità 200 e un tag di servizio che rappresenta l'ambito IP di Azure Front Door a un'app Web denominata ContosoSite che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="4fa1f-118">Esempio 4: Aggiungere una regola di restrizione di accesso a più indirizzi a un'app Web</span><span class="sxs-lookup"><span data-stu-id="4fa1f-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="4fa1f-119">Questo comando aggiunge una regola di restrizione di accesso con priorità 200 e due intervalli IP a un'app Web denominata ContosoSite che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="4fa1f-120">Esempio 5: Aggiungere una regola di restrizione di accesso con intestazione http a un'app Web</span><span class="sxs-lookup"><span data-stu-id="4fa1f-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="4fa1f-121">Questo comando aggiunge una regola di restrizione di accesso con priorità 400 per il tag di servizio AzureFrontDoor.Backend e limita ulteriormente l'accesso solo alle intestazioni http di determinati valori a un'app Web denominata ContosoSite che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4fa1f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fa1f-122">PARAMETERS</span></span>

### <span data-ttu-id="4fa1f-123">-Action</span><span class="sxs-lookup"><span data-stu-id="4fa1f-123">-Action</span></span>
<span data-ttu-id="4fa1f-124">Regola Consenti o Nega.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="4fa1f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa1f-125">-DefaultProfile</span></span>
<span data-ttu-id="4fa1f-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa1f-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fa1f-127">-Description</span></span>
<span data-ttu-id="4fa1f-128">Descrizione della restrizione di accesso.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="4fa1f-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="4fa1f-129">-HttpHeader</span></span>
<span data-ttu-id="4fa1f-130">Restrizioni per le intestazioni Http.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-130">Http header restrictions.</span></span> <span data-ttu-id="4fa1f-131">Esempio: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="4fa1f-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa1f-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fa1f-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="4fa1f-133">Specificare se deve essere convalidata la registrazione dell'endpoint di servizio in Subnet.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="4fa1f-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4fa1f-134">-IpAddress</span></span>
<span data-ttu-id="4fa1f-135">Intervallo IP Address v4 o v6 CIDR.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="4fa1f-136">Ad esempio: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="4fa1f-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="4fa1f-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4fa1f-137">-Name</span></span>
<span data-ttu-id="4fa1f-138">Nome regola</span><span class="sxs-lookup"><span data-stu-id="4fa1f-138">Rule Name</span></span>

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

### <span data-ttu-id="4fa1f-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fa1f-139">-PassThru</span></span>
<span data-ttu-id="4fa1f-140">Restituire l'oggetto configurazione della restrizione di accesso.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="4fa1f-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="4fa1f-141">-Priority</span></span>
<span data-ttu-id="4fa1f-142">Priorità della restrizione di accesso.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-142">Access Restriction priority.</span></span> <span data-ttu-id="4fa1f-143">Ad esempio: 500.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="4fa1f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa1f-144">-ResourceGroupName</span></span>
<span data-ttu-id="4fa1f-145">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4fa1f-145">Resource Group Name</span></span>

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

### <span data-ttu-id="4fa1f-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="4fa1f-146">-ServiceTag</span></span>
<span data-ttu-id="4fa1f-147">Nome del tag di servizio</span><span class="sxs-lookup"><span data-stu-id="4fa1f-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa1f-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="4fa1f-148">-SlotName</span></span>
<span data-ttu-id="4fa1f-149">Nome slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="4fa1f-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4fa1f-150">-SubnetId</span></span>
<span data-ttu-id="4fa1f-151">ResourceId della subnet.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="4fa1f-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4fa1f-152">-SubnetName</span></span>
<span data-ttu-id="4fa1f-153">Nome subnet.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="4fa1f-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="4fa1f-154">-TargetScmSite</span></span>
<span data-ttu-id="4fa1f-155">La regola è destinata al sito principale o al sito Scm.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="4fa1f-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4fa1f-156">-VirtualNetworkName</span></span>
<span data-ttu-id="4fa1f-157">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="4fa1f-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="4fa1f-158">-WebAppName</span></span>
<span data-ttu-id="4fa1f-159">Il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-159">The name of the web app.</span></span>

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

### <span data-ttu-id="4fa1f-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fa1f-160">-Confirm</span></span>
<span data-ttu-id="4fa1f-161">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fa1f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa1f-162">-WhatIf</span></span>
<span data-ttu-id="4fa1f-163">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fa1f-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fa1f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa1f-165">CommonParameters</span></span>
<span data-ttu-id="4fa1f-166">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa1f-167">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4fa1f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa1f-168">INPUT</span><span class="sxs-lookup"><span data-stu-id="4fa1f-168">INPUTS</span></span>

### <span data-ttu-id="4fa1f-169">System.String</span><span class="sxs-lookup"><span data-stu-id="4fa1f-169">System.String</span></span>

## <span data-ttu-id="4fa1f-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fa1f-170">OUTPUTS</span></span>

### <span data-ttu-id="4fa1f-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4fa1f-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="4fa1f-172">NOTE</span><span class="sxs-lookup"><span data-stu-id="4fa1f-172">NOTES</span></span>

## <span data-ttu-id="4fa1f-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fa1f-173">RELATED LINKS</span></span>

[<span data-ttu-id="4fa1f-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4fa1f-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="4fa1f-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4fa1f-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="4fa1f-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4fa1f-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
