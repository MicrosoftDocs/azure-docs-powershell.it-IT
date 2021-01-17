---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378976"
---
# <span data-ttu-id="5d685-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d685-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="5d685-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d685-102">SYNOPSIS</span></span>
<span data-ttu-id="5d685-103">Questo comando consente agli utenti di creare il pacchetto del profilo VPN in base alle impostazioni VPN preconfigurate nel gateway VPN, oltre ad alcune altre impostazioni che gli utenti potrebbero dover configurare, ad esempio alcuni certificati radice.</span><span class="sxs-lookup"><span data-stu-id="5d685-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="5d685-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d685-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d685-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d685-105">DESCRIPTION</span></span>
<span data-ttu-id="5d685-106">in questo modo gli utenti possono creare il pacchetto del profilo VPN in base alle impostazioni VPN preconfigurate nel gateway VPN, oltre ad alcune altre impostazioni che gli utenti potrebbero dover configurare, ad esempio alcuni certificati radice.</span><span class="sxs-lookup"><span data-stu-id="5d685-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="5d685-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d685-107">EXAMPLES</span></span>

### <span data-ttu-id="5d685-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d685-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="5d685-109">Questo cmdlet viene usato per creare un file zip del profilo client VPN per "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="5d685-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="5d685-110">Il profilo viene generato per un server RADIUS predefinito configurato per l'uso del metodo di autenticazione "EAPTLS" con il file di certificato VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="5d685-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="5d685-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d685-111">PARAMETERS</span></span>

### <span data-ttu-id="5d685-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="5d685-112">-AuthenticationMethod</span></span>
<span data-ttu-id="5d685-113">Il metodo di autenticazione può assumere valori EAPMSCHAPv2 o EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="5d685-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="5d685-114">Quando EAPMSCHAPv2 viene specificato, il cmdlet genera un programma di configurazione client per l'autenticazione di nome utente/password che usa il protocollo di autenticazione EAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="5d685-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="5d685-115">Se EAPTLS viene specificato, il cmdlet genera un programma di installazione della configurazione client per l'autenticazione dei certificati che usa il protocollo EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="5d685-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="5d685-116">L'opzione "EapTls" può essere usata sia per l'autenticazione dei certificati basata su RADIUS che per l'autenticazione di certificazione eseguita dal gateway di rete virtuale caricando la radice attendibile.</span><span class="sxs-lookup"><span data-stu-id="5d685-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="5d685-117">Il cmdlet rileva automaticamente le informazioni configurate.</span><span class="sxs-lookup"><span data-stu-id="5d685-117">The cmdlet automatically detects what is configured.</span></span>

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

### <span data-ttu-id="5d685-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="5d685-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="5d685-119">Elenco dei percorsi del certificato radice client</span><span class="sxs-lookup"><span data-stu-id="5d685-119">A list of client root certificate paths</span></span>

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

### <span data-ttu-id="5d685-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d685-120">-DefaultProfile</span></span>
<span data-ttu-id="5d685-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d685-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d685-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d685-122">-Name</span></span>
<span data-ttu-id="5d685-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5d685-123">The resource name.</span></span>

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

### <span data-ttu-id="5d685-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="5d685-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="5d685-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="5d685-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="5d685-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="5d685-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="5d685-127">Percorso del certificato radice del server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="5d685-127">Radius server root certificate path.</span></span> <span data-ttu-id="5d685-128">Si tratta di un parametro obbligatorio che deve essere specificato quando si usa EAP-TLS con l'autenticazione RADIUS.</span><span class="sxs-lookup"><span data-stu-id="5d685-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="5d685-129">Questo è il nome del percorso completo del file con estensione cer contenente il certificato radice RADIUS usato dal client per convalidare il server RADIUS durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5d685-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="5d685-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d685-130">-ResourceGroupName</span></span>
<span data-ttu-id="5d685-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d685-131">The resource group name.</span></span>

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

### <span data-ttu-id="5d685-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5d685-132">-Confirm</span></span>
<span data-ttu-id="5d685-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d685-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d685-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d685-134">-WhatIf</span></span>
<span data-ttu-id="5d685-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d685-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d685-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d685-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d685-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d685-137">CommonParameters</span></span>
<span data-ttu-id="5d685-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d685-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d685-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d685-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d685-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d685-140">INPUTS</span></span>

### <span data-ttu-id="5d685-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5d685-141">System.String</span></span>

### <span data-ttu-id="5d685-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="5d685-142">System.String[]</span></span>

## <span data-ttu-id="5d685-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d685-143">OUTPUTS</span></span>

### <span data-ttu-id="5d685-144">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="5d685-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="5d685-145">Note</span><span class="sxs-lookup"><span data-stu-id="5d685-145">NOTES</span></span>

## <span data-ttu-id="5d685-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d685-146">RELATED LINKS</span></span>

[<span data-ttu-id="5d685-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d685-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
