---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686961"
---
# <span data-ttu-id="ca6fb-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca6fb-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="ca6fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6fb-103">Aggiorna un servizio di gestione API di Azure</span><span class="sxs-lookup"><span data-stu-id="ca6fb-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca6fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca6fb-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca6fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca6fb-105">DESCRIPTION</span></span>

<span data-ttu-id="ca6fb-106">Il cmdlet **set-AzureRmApiManagement** aggiorna un servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="ca6fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca6fb-107">EXAMPLES</span></span>

### <span data-ttu-id="ca6fb-108">Esempio 1 ottenere un servizio di gestione delle API e ridimensionarlo in Premium e aggiungere un'area geografica</span><span class="sxs-lookup"><span data-stu-id="ca6fb-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="ca6fb-109">Questo esempio ottiene un'istanza di gestione delle API, la bilancia in cinque unità Premium e quindi aggiunge altre tre unità all'area Premium.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="ca6fb-110">Esempio 2: aggiornamento della distribuzione (VNET esterno)</span><span class="sxs-lookup"><span data-stu-id="ca6fb-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="ca6fb-111">Questo comando aggiorna una distribuzione di gestione delle API esistente e si unisce a un *VpnType* esterno.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="ca6fb-112">Esempio 3: creare e inizializzare un'istanza di PsApiManagementCustomHostNameConfiguration usando un segreto della risorsa del Vault</span><span class="sxs-lookup"><span data-stu-id="ca6fb-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="ca6fb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca6fb-113">PARAMETERS</span></span>

### <span data-ttu-id="ca6fb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca6fb-114">-AsJob</span></span>
<span data-ttu-id="ca6fb-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca6fb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca6fb-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ca6fb-116">-AssignIdentity</span></span>
<span data-ttu-id="ca6fb-117">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ca6fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6fb-118">-DefaultProfile</span></span>
<span data-ttu-id="ca6fb-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca6fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca6fb-120">-InputObject</span></span>
<span data-ttu-id="ca6fb-121">Istanza di ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="ca6fb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca6fb-122">-PassThru</span></span>
<span data-ttu-id="ca6fb-123">Invia l'aggiornamento di PsApiManagement alla pipeline se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="ca6fb-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca6fb-124">-Confirm</span></span>
<span data-ttu-id="ca6fb-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca6fb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca6fb-126">-WhatIf</span></span>
<span data-ttu-id="ca6fb-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca6fb-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca6fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6fb-129">CommonParameters</span></span>
<span data-ttu-id="ca6fb-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6fb-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca6fb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6fb-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca6fb-132">INPUTS</span></span>

### <span data-ttu-id="ca6fb-133">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca6fb-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="ca6fb-134">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca6fb-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ca6fb-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca6fb-135">OUTPUTS</span></span>

### <span data-ttu-id="ca6fb-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca6fb-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ca6fb-137">Note</span><span class="sxs-lookup"><span data-stu-id="ca6fb-137">NOTES</span></span>

## <span data-ttu-id="ca6fb-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca6fb-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca6fb-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca6fb-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ca6fb-140">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca6fb-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ca6fb-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ca6fb-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
