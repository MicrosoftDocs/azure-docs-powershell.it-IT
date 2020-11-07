---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: dbc5a10865874830c2f06a59f799722f61a3e9e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675916"
---
# <span data-ttu-id="d06ac-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d06ac-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="d06ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d06ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d06ac-103">Aggiorna un servizio di gestione API di Azure</span><span class="sxs-lookup"><span data-stu-id="d06ac-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="d06ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d06ac-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d06ac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d06ac-105">DESCRIPTION</span></span>

<span data-ttu-id="d06ac-106">Il cmdlet **set-AzApiManagement** aggiorna un servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="d06ac-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="d06ac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d06ac-107">EXAMPLES</span></span>

### <span data-ttu-id="d06ac-108">Esempio 1 ottenere un servizio di gestione delle API e ridimensionarlo in Premium e aggiungere un'area geografica</span><span class="sxs-lookup"><span data-stu-id="d06ac-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="d06ac-109">Questo esempio ottiene un'istanza di gestione delle API, la bilancia in cinque unità Premium e quindi aggiunge altre tre unità all'area Premium.</span><span class="sxs-lookup"><span data-stu-id="d06ac-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="d06ac-110">Esempio 2: aggiornamento della distribuzione (VNET esterno)</span><span class="sxs-lookup"><span data-stu-id="d06ac-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="d06ac-111">Questo comando aggiorna una distribuzione di gestione delle API esistente e si unisce a un *VpnType* esterno.</span><span class="sxs-lookup"><span data-stu-id="d06ac-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="d06ac-112">Esempio 3: creare e inizializzare un'istanza di PsApiManagementCustomHostNameConfiguration usando un segreto della risorsa del Vault</span><span class="sxs-lookup"><span data-stu-id="d06ac-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -AssignIdentity
```

### <span data-ttu-id="d06ac-113">Esempio 4: aggiornare la posta elettronica di Publisher, NotificationSender la posta elettronica e il nome dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="d06ac-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="d06ac-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d06ac-114">PARAMETERS</span></span>

### <span data-ttu-id="d06ac-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d06ac-115">-AsJob</span></span>
<span data-ttu-id="d06ac-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d06ac-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d06ac-117">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d06ac-117">-AssignIdentity</span></span>
<span data-ttu-id="d06ac-118">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d06ac-118">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d06ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06ac-119">-DefaultProfile</span></span>
<span data-ttu-id="d06ac-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d06ac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d06ac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d06ac-121">-InputObject</span></span>
<span data-ttu-id="d06ac-122">Istanza di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d06ac-122">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="d06ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d06ac-123">-PassThru</span></span>
<span data-ttu-id="d06ac-124">Invia l'aggiornamento di PsApiManagement alla pipeline se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="d06ac-124">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="d06ac-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d06ac-125">-Confirm</span></span>
<span data-ttu-id="d06ac-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d06ac-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d06ac-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d06ac-127">-WhatIf</span></span>
<span data-ttu-id="d06ac-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d06ac-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d06ac-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d06ac-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d06ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06ac-130">CommonParameters</span></span>
<span data-ttu-id="d06ac-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d06ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06ac-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d06ac-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06ac-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d06ac-133">INPUTS</span></span>

### <span data-ttu-id="d06ac-134">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d06ac-134">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d06ac-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d06ac-135">OUTPUTS</span></span>

### <span data-ttu-id="d06ac-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d06ac-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d06ac-137">Note</span><span class="sxs-lookup"><span data-stu-id="d06ac-137">NOTES</span></span>

## <span data-ttu-id="d06ac-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d06ac-138">RELATED LINKS</span></span>

[<span data-ttu-id="d06ac-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d06ac-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="d06ac-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d06ac-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="d06ac-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d06ac-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
