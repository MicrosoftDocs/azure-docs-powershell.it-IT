---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189631"
---
# <span data-ttu-id="eaf03-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaf03-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="eaf03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf03-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf03-103">Questo comando consente agli utenti di creare il pacchetto di profili Vpn in base alle impostazioni VPN preconfigurte nel gateway VPN, oltre ad alcune impostazioni aggiuntive che gli utenti potrebbero dover configurare, ad esempio alcuni certificati radice.</span><span class="sxs-lookup"><span data-stu-id="eaf03-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="eaf03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eaf03-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaf03-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eaf03-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf03-106">in questo modo gli utenti possono creare il pacchetto di profili Vpn in base alle impostazioni VPN preconfigurte nel gateway VPN, oltre ad alcune impostazioni aggiuntive che gli utenti potrebbero dover configurare, ad esempio alcuni certificati radice.</span><span class="sxs-lookup"><span data-stu-id="eaf03-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="eaf03-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eaf03-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf03-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eaf03-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="eaf03-109">Questo cmdlet viene usato per creare un file ZIP del profilo client VPN per "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="eaf03-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="eaf03-110">Il profilo viene generato per un server di raggio preconfigurato configurato per l'uso del metodo di autenticazione "EAPTLS" con il file di certificato VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="eaf03-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="eaf03-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaf03-111">PARAMETERS</span></span>

### <span data-ttu-id="eaf03-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="eaf03-112">-AuthenticationMethod</span></span>
<span data-ttu-id="eaf03-113">Il metodo di autenticazione può assumere valori EAPMSCHAPv2 o EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="eaf03-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="eaf03-114">Quando si specifica EAPMSCHAPv2, il cmdlet genera un programma di installazione di configurazione client per l'autenticazione nome utente/password che usa EAP-MSCHAPv2 di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="eaf03-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="eaf03-115">Se si specifica EAPTLS, il cmdlet genera un programma di installazione della configurazione client per l'autenticazione del certificato che usa il protocollo EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="eaf03-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="eaf03-116">L'opzione "EapTls" può essere usata sia per l'autenticazione basata su certificato basata su RADIUS che per l'autenticazione della certificazione eseguita da Gateway di rete virtuale caricando la radice attendibile.</span><span class="sxs-lookup"><span data-stu-id="eaf03-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="eaf03-117">Il cmdlet rileva automaticamente ciò che è configurato.</span><span class="sxs-lookup"><span data-stu-id="eaf03-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf03-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="eaf03-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="eaf03-119">Elenco dei percorsi dei certificati radice client</span><span class="sxs-lookup"><span data-stu-id="eaf03-119">A list of client root certificate paths</span></span>

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

### <span data-ttu-id="eaf03-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf03-120">-DefaultProfile</span></span>
<span data-ttu-id="eaf03-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf03-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaf03-122">-Name</span><span class="sxs-lookup"><span data-stu-id="eaf03-122">-Name</span></span>
<span data-ttu-id="eaf03-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eaf03-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf03-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="eaf03-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="eaf03-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="eaf03-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf03-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="eaf03-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="eaf03-127">Percorso certificato radice del server di raggio.</span><span class="sxs-lookup"><span data-stu-id="eaf03-127">Radius server root certificate path.</span></span> <span data-ttu-id="eaf03-128">Questo è un parametro obbligatorio che deve essere specificato quando si usa EAP-TLS con autenticazione RADIUS.</span><span class="sxs-lookup"><span data-stu-id="eaf03-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="eaf03-129">Nome percorso completo del file CER contenente il certificato radice RADIUS utilizzato dal client per convalidare il server RADIUS durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="eaf03-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf03-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf03-130">-ResourceGroupName</span></span>
<span data-ttu-id="eaf03-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eaf03-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf03-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaf03-132">-Confirm</span></span>
<span data-ttu-id="eaf03-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaf03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf03-134">-WhatIf</span></span>
<span data-ttu-id="eaf03-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eaf03-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaf03-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eaf03-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf03-137">CommonParameters</span></span>
<span data-ttu-id="eaf03-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf03-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf03-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf03-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="eaf03-140">INPUTS</span></span>

### <span data-ttu-id="eaf03-141">System.String</span><span class="sxs-lookup"><span data-stu-id="eaf03-141">System.String</span></span>

### <span data-ttu-id="eaf03-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="eaf03-142">System.String[]</span></span>

## <span data-ttu-id="eaf03-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eaf03-143">OUTPUTS</span></span>

### <span data-ttu-id="eaf03-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="eaf03-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="eaf03-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="eaf03-145">NOTES</span></span>

## <span data-ttu-id="eaf03-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eaf03-146">RELATED LINKS</span></span>

[<span data-ttu-id="eaf03-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaf03-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
