---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354724"
---
# <span data-ttu-id="6f029-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="6f029-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="6f029-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f029-102">SYNOPSIS</span></span>
<span data-ttu-id="6f029-103">Aggiunge una regola di restiction di Access a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f029-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="6f029-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f029-104">SYNTAX</span></span>

### <span data-ttu-id="6f029-105">IpAddressParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6f029-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f029-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f029-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f029-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f029-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f029-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f029-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f029-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f029-109">DESCRIPTION</span></span>
<span data-ttu-id="6f029-110">Il cmdlet **Add-AzWebAppAccessRestrictionRule** aggiunge una regola di restrizione di Access a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f029-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="6f029-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f029-111">EXAMPLES</span></span>

### <span data-ttu-id="6f029-112">Esempio 1: aggiungere la regola di restrizione dell'accesso IpAddress a un'app Web</span><span class="sxs-lookup"><span data-stu-id="6f029-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="6f029-113">Questo comando aggiunge una regola di restrizione di Access con priorità 200 e un intervallo IP a un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6f029-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6f029-114">Esempio 2: aggiungere la regola di restrizione di accesso al servizio subnet in un'app Web</span><span class="sxs-lookup"><span data-stu-id="6f029-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="6f029-115">Questo comando aggiunge una regola di restrizione di Access con priorità 300 e subnet appgw-subnet in Corp-VNET a un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6f029-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6f029-116">Esempio 3: aggiungere la regola di restrizione di accesso di ServiceTag a un'app Web</span><span class="sxs-lookup"><span data-stu-id="6f029-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="6f029-117">Questo comando aggiunge una regola di restrizione di Access con priorità 200 e un tag di servizio che rappresenta l'ambito IP di Azure front door in un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6f029-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6f029-118">Esempio 4: aggiungere la regola di restrizione dell'accesso multiindirizzo a un'app Web</span><span class="sxs-lookup"><span data-stu-id="6f029-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="6f029-119">Questo comando aggiunge una regola di restrizione di Access con priorità 200 e due intervalli di indirizzi IP a un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6f029-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6f029-120">Esempio 5: aggiungere la regola di restrizione di Access con l'intestazione HTTP a un'app Web</span><span class="sxs-lookup"><span data-stu-id="6f029-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="6f029-121">Questo comando aggiunge una regola di restrizione di Access con priorità 400 per il tag Service AzureFrontDoor. backend e limita ulteriormente l'accesso solo alle intestazioni HTTP di determinati valori a un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6f029-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6f029-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f029-122">PARAMETERS</span></span>

### <span data-ttu-id="6f029-123">-Azione</span><span class="sxs-lookup"><span data-stu-id="6f029-123">-Action</span></span>
<span data-ttu-id="6f029-124">Consentire o negare la regola.</span><span class="sxs-lookup"><span data-stu-id="6f029-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="6f029-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f029-125">-DefaultProfile</span></span>
<span data-ttu-id="6f029-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f029-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f029-127">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f029-127">-Description</span></span>
<span data-ttu-id="6f029-128">Descrizione della restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="6f029-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="6f029-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="6f029-129">-HttpHeader</span></span>
<span data-ttu-id="6f029-130">Restrizioni dell'intestazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="6f029-130">Http header restrictions.</span></span> <span data-ttu-id="6f029-131">Esempio:-HttpHeader @ {' x-Azure-fdid ' =' 7acacb02-47ea-4cd4-B568-5e880e72582e '; ' x-Forwarded-host ' =' www.contoso.com ',' app.contoso.com '}</span><span class="sxs-lookup"><span data-stu-id="6f029-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="6f029-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f029-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="6f029-133">Specificare se la registrazione dell'endpoint del servizio nella subnet deve essere convalidata.</span><span class="sxs-lookup"><span data-stu-id="6f029-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="6f029-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="6f029-134">-IpAddress</span></span>
<span data-ttu-id="6f029-135">Indirizzo IP v4 o gamma CIDR V6.</span><span class="sxs-lookup"><span data-stu-id="6f029-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="6f029-136">Ad esempio: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="6f029-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="6f029-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f029-137">-Name</span></span>
<span data-ttu-id="6f029-138">Nome regola</span><span class="sxs-lookup"><span data-stu-id="6f029-138">Rule Name</span></span>

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

### <span data-ttu-id="6f029-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f029-139">-PassThru</span></span>
<span data-ttu-id="6f029-140">Restituisce l'oggetto di configurazione di restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="6f029-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="6f029-141">-Priorità</span><span class="sxs-lookup"><span data-stu-id="6f029-141">-Priority</span></span>
<span data-ttu-id="6f029-142">Priorità restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="6f029-142">Access Restriction priority.</span></span> <span data-ttu-id="6f029-143">Ad esempio: 500.</span><span class="sxs-lookup"><span data-stu-id="6f029-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="6f029-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f029-144">-ResourceGroupName</span></span>
<span data-ttu-id="6f029-145">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6f029-145">Resource Group Name</span></span>

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

### <span data-ttu-id="6f029-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="6f029-146">-ServiceTag</span></span>
<span data-ttu-id="6f029-147">Nome del tag servizio</span><span class="sxs-lookup"><span data-stu-id="6f029-147">Name of Service Tag</span></span>

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

### <span data-ttu-id="6f029-148">-Slotname</span><span class="sxs-lookup"><span data-stu-id="6f029-148">-SlotName</span></span>
<span data-ttu-id="6f029-149">Nome dello slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6f029-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="6f029-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6f029-150">-SubnetId</span></span>
<span data-ttu-id="6f029-151">ResourceId della subnet.</span><span class="sxs-lookup"><span data-stu-id="6f029-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="6f029-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6f029-152">-SubnetName</span></span>
<span data-ttu-id="6f029-153">Nome della subnet.</span><span class="sxs-lookup"><span data-stu-id="6f029-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="6f029-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="6f029-154">-TargetScmSite</span></span>
<span data-ttu-id="6f029-155">La regola è destinata al sito principale o all'area SCM.</span><span class="sxs-lookup"><span data-stu-id="6f029-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="6f029-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6f029-156">-VirtualNetworkName</span></span>
<span data-ttu-id="6f029-157">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f029-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="6f029-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="6f029-158">-WebAppName</span></span>
<span data-ttu-id="6f029-159">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="6f029-159">The name of the web app.</span></span>

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

### <span data-ttu-id="6f029-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6f029-160">-Confirm</span></span>
<span data-ttu-id="6f029-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f029-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f029-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f029-162">-WhatIf</span></span>
<span data-ttu-id="6f029-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f029-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f029-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f029-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f029-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f029-165">CommonParameters</span></span>
<span data-ttu-id="6f029-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f029-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f029-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f029-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f029-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f029-168">INPUTS</span></span>

### <span data-ttu-id="6f029-169">System. String</span><span class="sxs-lookup"><span data-stu-id="6f029-169">System.String</span></span>

## <span data-ttu-id="6f029-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f029-170">OUTPUTS</span></span>

### <span data-ttu-id="6f029-171">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6f029-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="6f029-172">Note</span><span class="sxs-lookup"><span data-stu-id="6f029-172">NOTES</span></span>

## <span data-ttu-id="6f029-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f029-173">RELATED LINKS</span></span>

[<span data-ttu-id="6f029-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6f029-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="6f029-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6f029-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="6f029-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="6f029-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
