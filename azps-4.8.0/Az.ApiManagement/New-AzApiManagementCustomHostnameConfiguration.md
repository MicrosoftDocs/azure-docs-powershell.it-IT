---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031460"
---
# <span data-ttu-id="74276-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="74276-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="74276-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74276-102">SYNOPSIS</span></span>
<span data-ttu-id="74276-103">Crea un'istanza di `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="74276-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="74276-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74276-104">SYNTAX</span></span>

### <span data-ttu-id="74276-105">NoChangeCertificate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74276-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74276-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="74276-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74276-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="74276-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74276-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74276-108">DESCRIPTION</span></span>
<span data-ttu-id="74276-109">Il cmdlet **New-AzApiManagementCustomHostnameConfiguration** è un comando helper che crea un'istanza di **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="74276-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="74276-110">Questo comando viene usato con il cmdlet New-AzApiManagement e Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="74276-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="74276-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74276-111">EXAMPLES</span></span>

### <span data-ttu-id="74276-112">Esempio 1: creare e inizializzare un'istanza di PsApiManagementCustomHostNameConfiguration usando un certificato SSL da un file</span><span class="sxs-lookup"><span data-stu-id="74276-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="74276-113">Questo comando crea e Inizializza un'istanza di **PsApiManagementCustomHostNameConfiguration** per Portal.</span><span class="sxs-lookup"><span data-stu-id="74276-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="74276-114">Crea quindi un nuovo servizio ApiManagement con la configurazione personalizzata del nome host.</span><span class="sxs-lookup"><span data-stu-id="74276-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="74276-115">Esempio 2: creare e inizializzare un'istanza di PsApiManagementCustomHostNameConfiguration usando un segreto della risorsa del Vault</span><span class="sxs-lookup"><span data-stu-id="74276-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="74276-116">Questo comando crea e Inizializza un'istanza di **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="74276-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="74276-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74276-117">PARAMETERS</span></span>

### <span data-ttu-id="74276-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74276-118">-DefaultProfile</span></span>
<span data-ttu-id="74276-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74276-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74276-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="74276-120">-DefaultSslBinding</span></span>
<span data-ttu-id="74276-121">Determina se il valore è un segreto e deve essere crittografato o meno.</span><span class="sxs-lookup"><span data-stu-id="74276-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="74276-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74276-122">This parameter is optional.</span></span>
<span data-ttu-id="74276-123">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="74276-123">Default Value is false.</span></span>

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

### <span data-ttu-id="74276-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="74276-124">-Hostname</span></span>
<span data-ttu-id="74276-125">Nome host personalizzato</span><span class="sxs-lookup"><span data-stu-id="74276-125">Custom Hostname</span></span>

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

### <span data-ttu-id="74276-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="74276-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="74276-127">Configurazione del certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="74276-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="74276-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="74276-128">-HostnameType</span></span>
<span data-ttu-id="74276-129">Tipo hostname</span><span class="sxs-lookup"><span data-stu-id="74276-129">Hostname Type</span></span>

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

### <span data-ttu-id="74276-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="74276-130">-KeyVaultId</span></span>
<span data-ttu-id="74276-131">KeyVaultId al segreto che archivia il certificato SSL personalizzato.</span><span class="sxs-lookup"><span data-stu-id="74276-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="74276-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="74276-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="74276-133">Determina se il valore è un segreto e deve essere crittografato o meno.</span><span class="sxs-lookup"><span data-stu-id="74276-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="74276-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74276-134">This parameter is optional.</span></span>
<span data-ttu-id="74276-135">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="74276-135">Default Value is false.</span></span>

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

### <span data-ttu-id="74276-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="74276-136">-PfxPassword</span></span>
<span data-ttu-id="74276-137">Password per il file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="74276-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="74276-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="74276-138">-PfxPath</span></span>
<span data-ttu-id="74276-139">Percorso di un file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="74276-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="74276-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74276-140">CommonParameters</span></span>
<span data-ttu-id="74276-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74276-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74276-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74276-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74276-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74276-143">INPUTS</span></span>

### <span data-ttu-id="74276-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="74276-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="74276-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74276-145">OUTPUTS</span></span>

### <span data-ttu-id="74276-146">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="74276-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="74276-147">Note</span><span class="sxs-lookup"><span data-stu-id="74276-147">NOTES</span></span>

## <span data-ttu-id="74276-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74276-148">RELATED LINKS</span></span>

[<span data-ttu-id="74276-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74276-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="74276-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74276-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)