---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176502"
---
# <span data-ttu-id="c8474-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8474-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="c8474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8474-102">SYNOPSIS</span></span>
<span data-ttu-id="c8474-103">Crea un'istanza di `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="c8474-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="c8474-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8474-104">SYNTAX</span></span>

### <span data-ttu-id="c8474-105">NoChangeCertificate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8474-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8474-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="c8474-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8474-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="c8474-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8474-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8474-108">DESCRIPTION</span></span>
<span data-ttu-id="c8474-109">Il cmdlet **New-AzApiManagementCustomHostnameConfiguration** è un comando helper che crea un'istanza di **PsApiManagementCustomHostNameConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c8474-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="c8474-110">Questo comando viene usato con il cmdlet New-AzApiManagement e Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8474-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="c8474-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8474-111">EXAMPLES</span></span>

### <span data-ttu-id="c8474-112">Esempio 1: Creare e inizializzare un'istanza di PsApiManagementCustomHostNameConfiguration usando un certificato Ssl da file</span><span class="sxs-lookup"><span data-stu-id="c8474-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="c8474-113">Questo comando crea e inizializza un'istanza **di PsApiManagementCustomHostNameConfiguration** per il portale.</span><span class="sxs-lookup"><span data-stu-id="c8474-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="c8474-114">Viene quindi creato un nuovo servizio ApiManagement con configurazione di nomi host personalizzati.</span><span class="sxs-lookup"><span data-stu-id="c8474-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="c8474-115">Esempio 2: Creare e inizializzare un'istanza di PsApiManagementCustomHostNameConfiguration usando un segreto dalla risorsa KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8474-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="c8474-116">Questo comando crea e inizializza un'istanza **di PsApiManagementCustomHostNameConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c8474-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="c8474-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8474-117">PARAMETERS</span></span>

### <span data-ttu-id="c8474-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8474-118">-DefaultProfile</span></span>
<span data-ttu-id="c8474-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8474-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8474-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="c8474-120">-DefaultSslBinding</span></span>
<span data-ttu-id="c8474-121">Determina se il valore è un segreto e deve essere crittografato o meno.</span><span class="sxs-lookup"><span data-stu-id="c8474-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="c8474-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c8474-122">This parameter is optional.</span></span>
<span data-ttu-id="c8474-123">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="c8474-123">Default Value is false.</span></span>

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

### <span data-ttu-id="c8474-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="c8474-124">-Hostname</span></span>
<span data-ttu-id="c8474-125">Nome host personalizzato</span><span class="sxs-lookup"><span data-stu-id="c8474-125">Custom Hostname</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8474-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="c8474-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="c8474-127">Configurazione certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="c8474-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8474-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="c8474-128">-HostnameType</span></span>
<span data-ttu-id="c8474-129">Tipo di nome host</span><span class="sxs-lookup"><span data-stu-id="c8474-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8474-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c8474-130">-KeyVaultId</span></span>
<span data-ttu-id="c8474-131">KeyVaultId per il segreto in cui è archiviato il certificato SSL personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c8474-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8474-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c8474-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="c8474-133">Determina se il valore è un segreto e deve essere crittografato o meno.</span><span class="sxs-lookup"><span data-stu-id="c8474-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="c8474-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c8474-134">This parameter is optional.</span></span>
<span data-ttu-id="c8474-135">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="c8474-135">Default Value is false.</span></span>

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

### <span data-ttu-id="c8474-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="c8474-136">-PfxPassword</span></span>
<span data-ttu-id="c8474-137">Password per il file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="c8474-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8474-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="c8474-138">-PfxPath</span></span>
<span data-ttu-id="c8474-139">Percorso di un file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="c8474-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8474-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8474-140">CommonParameters</span></span>
<span data-ttu-id="c8474-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8474-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8474-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8474-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8474-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8474-143">INPUTS</span></span>

### <span data-ttu-id="c8474-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="c8474-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="c8474-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8474-145">OUTPUTS</span></span>

### <span data-ttu-id="c8474-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8474-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="c8474-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8474-147">NOTES</span></span>

## <span data-ttu-id="c8474-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8474-148">RELATED LINKS</span></span>

[<span data-ttu-id="c8474-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8474-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="c8474-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c8474-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)