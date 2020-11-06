---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: d48d1913a30fc03ca0ebaf86195b981a6ebe70fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521471"
---
# <span data-ttu-id="3058c-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3058c-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="3058c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3058c-102">SYNOPSIS</span></span>
<span data-ttu-id="3058c-103">Imposta una configurazione personalizzata del nome host per un portale o un proxy del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3058c-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3058c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3058c-104">SYNTAX</span></span>

### <span data-ttu-id="3058c-105">SetSpecificService (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3058c-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3058c-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="3058c-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3058c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3058c-107">DESCRIPTION</span></span>
<span data-ttu-id="3058c-108">Il cmdlet **set-AzureRmApiManagementHostnames** applica una configurazione hostname personalizzata per un portale o un proxy del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3058c-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="3058c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3058c-109">EXAMPLES</span></span>

### <span data-ttu-id="3058c-110">Esempio 1: impostare la configurazione personalizzata del nome host per un proxy e un portale</span><span class="sxs-lookup"><span data-stu-id="3058c-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="3058c-111">Questo comando imposta la configurazione personalizzata del nome host per proxy e portale.</span><span class="sxs-lookup"><span data-stu-id="3058c-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="3058c-112">Esempio 2: configurare un nome host personalizzato per un proxy e un portale</span><span class="sxs-lookup"><span data-stu-id="3058c-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="3058c-113">Questo esempio configura un nome host personalizzato per proxy e portale.</span><span class="sxs-lookup"><span data-stu-id="3058c-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="3058c-114">È necessario importare i certificati corrispondenti e quindi applicare i nomi host personalizzati.</span><span class="sxs-lookup"><span data-stu-id="3058c-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="3058c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3058c-115">PARAMETERS</span></span>

### <span data-ttu-id="3058c-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3058c-116">-ApiManagement</span></span>
<span data-ttu-id="3058c-117">Specifica l'istanza di **PsApiManagement** a cui questo cmdlet ottiene i parametri *PortalHostnameConfiguration* e *ProxyHostnameConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="3058c-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3058c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3058c-118">-DefaultProfile</span></span>
<span data-ttu-id="3058c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3058c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3058c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3058c-120">-Name</span></span>
<span data-ttu-id="3058c-121">Specifica il nome dell'istanza di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3058c-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3058c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3058c-122">-PassThru</span></span>
<span data-ttu-id="3058c-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3058c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3058c-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3058c-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3058c-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3058c-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="3058c-126">Specifica la configurazione del nome host del portale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3058c-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="3058c-127">Il passaggio di $null al cmdlet imposta il nome host predefinito.</span><span class="sxs-lookup"><span data-stu-id="3058c-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3058c-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3058c-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="3058c-129">Specifica la configurazione del nome host proxy personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3058c-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="3058c-130">Passando $null imposta il nome host predefinito.</span><span class="sxs-lookup"><span data-stu-id="3058c-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3058c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3058c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3058c-132">Specifica il nome del gruppo di risorse in cui è presente l'istanza di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3058c-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3058c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3058c-133">CommonParameters</span></span>
<span data-ttu-id="3058c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3058c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3058c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3058c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3058c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3058c-136">INPUTS</span></span>

### <span data-ttu-id="3058c-137">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3058c-137">PsApiManagement</span></span>
<span data-ttu-id="3058c-138">Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3058c-138">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="3058c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3058c-139">OUTPUTS</span></span>

### <span data-ttu-id="3058c-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3058c-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3058c-141">Note</span><span class="sxs-lookup"><span data-stu-id="3058c-141">NOTES</span></span>

## <span data-ttu-id="3058c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3058c-142">RELATED LINKS</span></span>

[<span data-ttu-id="3058c-143">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3058c-143">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="3058c-144">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3058c-144">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


