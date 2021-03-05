---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: 3f1ab16dd6bf8dd264bdb4e4427d45197feace7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971581"
---
# <span data-ttu-id="ac1d2-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ac1d2-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="ac1d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1d2-103">Aggiorna un servizio di gestione api di Azure</span><span class="sxs-lookup"><span data-stu-id="ac1d2-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="ac1d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac1d2-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac1d2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac1d2-105">DESCRIPTION</span></span>

<span data-ttu-id="ac1d2-106">Il cmdlet **Set-AzApiManagement aggiorna** un servizio di gestione DELLE API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="ac1d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac1d2-107">EXAMPLES</span></span>

### <span data-ttu-id="ac1d2-108">Esempio 1: Ottenere un servizio di gestione DELLE API e ridimensionarlo su Premium e aggiungere un'area geografica</span><span class="sxs-lookup"><span data-stu-id="ac1d2-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="ac1d2-109">Questo esempio ottiene un'istanza di Gestione Api, la ridimensiona a cinque unità premium e quindi aggiunge altre tre unità all'area premium.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="ac1d2-110">Esempio 2: Aggiornare la distribuzione (VNET esterna)</span><span class="sxs-lookup"><span data-stu-id="ac1d2-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="ac1d2-111">Questo comando aggiorna una distribuzione esistente di Gestione API e si unisce a un *VpnType esterno.*</span><span class="sxs-lookup"><span data-stu-id="ac1d2-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="ac1d2-112">Esempio 3: Creare e inizializzare un'istanza di PsApiManagementCustomHostNameConfiguration usando un segreto dalla risorsa KeyVault</span><span class="sxs-lookup"><span data-stu-id="ac1d2-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="ac1d2-113">Esempio 4: Aggiornare la posta elettronica di Publisher, l'indirizzo di posta elettronica di NotificationSender e il nome dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="ac1d2-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="ac1d2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac1d2-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac1d2-115">-AsJob</span></span>
<span data-ttu-id="ac1d2-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ac1d2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac1d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1d2-117">-DefaultProfile</span></span>
<span data-ttu-id="ac1d2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac1d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac1d2-119">-InputObject</span></span>
<span data-ttu-id="ac1d2-120">Istanza Di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-120">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1d2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac1d2-121">-PassThru</span></span>
<span data-ttu-id="ac1d2-122">Invia PsApiManagement aggiornato alla pipeline se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="ac1d2-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ac1d2-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="ac1d2-124">Generare e assegnare un'identità di Azure Active Directory per questo server per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ac1d2-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ac1d2-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="ac1d2-126">Assegnare identità utente a questo server per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1d2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac1d2-127">-Confirm</span></span>
<span data-ttu-id="ac1d2-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1d2-129">-WhatIf</span></span>
<span data-ttu-id="ac1d2-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac1d2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1d2-132">CommonParameters</span></span>
<span data-ttu-id="ac1d2-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1d2-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac1d2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1d2-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac1d2-135">INPUTS</span></span>

### <span data-ttu-id="ac1d2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ac1d2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ac1d2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac1d2-137">OUTPUTS</span></span>

### <span data-ttu-id="ac1d2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ac1d2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ac1d2-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac1d2-139">NOTES</span></span>

## <span data-ttu-id="ac1d2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac1d2-140">RELATED LINKS</span></span>

[<span data-ttu-id="ac1d2-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ac1d2-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="ac1d2-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ac1d2-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="ac1d2-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ac1d2-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
