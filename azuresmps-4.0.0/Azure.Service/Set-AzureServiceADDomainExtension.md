---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029510"
---
# <span data-ttu-id="65b3d-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="65b3d-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="65b3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="65b3d-103">Abilita un'estensione del dominio Active Directory per un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="65b3d-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="65b3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65b3d-104">SYNTAX</span></span>

### <span data-ttu-id="65b3d-105">JoinDomainUsingEnumOptions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65b3d-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="65b3d-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="65b3d-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="65b3d-107">Workgroup</span><span class="sxs-lookup"><span data-stu-id="65b3d-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="65b3d-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="65b3d-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="65b3d-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="65b3d-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="65b3d-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="65b3d-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="65b3d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65b3d-111">DESCRIPTION</span></span>
<span data-ttu-id="65b3d-112">Il cmdlet **set-AzureServiceADDomainExtension** Abilita un'estensione di dominio Active Directory per un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="65b3d-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="65b3d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65b3d-113">EXAMPLES</span></span>

### <span data-ttu-id="65b3d-114">1:</span><span class="sxs-lookup"><span data-stu-id="65b3d-114">1:</span></span>
```

```

## <span data-ttu-id="65b3d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65b3d-115">PARAMETERS</span></span>

### <span data-ttu-id="65b3d-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="65b3d-116">-CertificateThumbprint</span></span>
<span data-ttu-id="65b3d-117">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="65b3d-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="65b3d-118">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="65b3d-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="65b3d-119">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="65b3d-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-120">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="65b3d-120">-Credential</span></span>
<span data-ttu-id="65b3d-121">Specifica le credenziali per l'aggiunta del dominio di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="65b3d-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="65b3d-122">Le credenziali includono un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="65b3d-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-123">-DomainName</span><span class="sxs-lookup"><span data-stu-id="65b3d-123">-DomainName</span></span>
<span data-ttu-id="65b3d-124">Specifica il nome di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="65b3d-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="65b3d-125">-ExtensionId</span></span>
<span data-ttu-id="65b3d-126">Specifica l'ID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="65b3d-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="65b3d-127">-InformationAction</span></span>
<span data-ttu-id="65b3d-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="65b3d-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="65b3d-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="65b3d-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="65b3d-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="65b3d-130">Continue</span></span>
- <span data-ttu-id="65b3d-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="65b3d-131">Ignore</span></span>
- <span data-ttu-id="65b3d-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="65b3d-132">Inquire</span></span>
- <span data-ttu-id="65b3d-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="65b3d-133">SilentlyContinue</span></span>
- <span data-ttu-id="65b3d-134">Stop</span><span class="sxs-lookup"><span data-stu-id="65b3d-134">Stop</span></span>
- <span data-ttu-id="65b3d-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="65b3d-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="65b3d-136">-InformationVariable</span></span>
<span data-ttu-id="65b3d-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="65b3d-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="65b3d-138">-JoinOption</span></span>
<span data-ttu-id="65b3d-139">Specifica l'enumerazione dell'opzione join.</span><span class="sxs-lookup"><span data-stu-id="65b3d-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-140">-Opzioni</span><span class="sxs-lookup"><span data-stu-id="65b3d-140">-Options</span></span>
<span data-ttu-id="65b3d-141">Specifica l'opzione Unisci interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="65b3d-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="65b3d-142">-OUPath</span></span>
<span data-ttu-id="65b3d-143">Specifica il percorso dell'unità organizzativa per l'operazione di join del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="65b3d-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="65b3d-144">-Profile</span></span>
<span data-ttu-id="65b3d-145">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b3d-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65b3d-146">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="65b3d-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-147">-Riavviare</span><span class="sxs-lookup"><span data-stu-id="65b3d-147">-Restart</span></span>
<span data-ttu-id="65b3d-148">Specifica se riavviare il computer se l'operazione di join riesce.</span><span class="sxs-lookup"><span data-stu-id="65b3d-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-149">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="65b3d-149">-Role</span></span>
<span data-ttu-id="65b3d-150">Specifica una matrice facoltativa di ruoli per cui specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="65b3d-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="65b3d-151">Se non viene specificata la configurazione del dominio Active Directory viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="65b3d-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="65b3d-152">-ServiceName</span></span>
<span data-ttu-id="65b3d-153">Specifica il nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="65b3d-153">Specifies the cloud service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-154">-Slot</span><span class="sxs-lookup"><span data-stu-id="65b3d-154">-Slot</span></span>
<span data-ttu-id="65b3d-155">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="65b3d-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="65b3d-156">I valori accettabili per questo parametro sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="65b3d-156">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="65b3d-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="65b3d-158">Specifica un algoritmo di hash dell'identificazione digitale usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="65b3d-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="65b3d-159">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="65b3d-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="65b3d-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="65b3d-161">Specifica le credenziali (nome utente e password) per la dispartecipazione al dominio di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="65b3d-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-162">-Versione</span><span class="sxs-lookup"><span data-stu-id="65b3d-162">-Version</span></span>
<span data-ttu-id="65b3d-163">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="65b3d-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-164">-Workgroup</span><span class="sxs-lookup"><span data-stu-id="65b3d-164">-WorkgroupName</span></span>
<span data-ttu-id="65b3d-165">Specifica il nome del gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="65b3d-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="65b3d-166">-X509Certificate</span></span>
<span data-ttu-id="65b3d-167">Specifica un certificato X509 che, se specificato, verrà caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="65b3d-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b3d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b3d-168">CommonParameters</span></span>
<span data-ttu-id="65b3d-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b3d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b3d-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b3d-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b3d-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65b3d-171">INPUTS</span></span>

## <span data-ttu-id="65b3d-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65b3d-172">OUTPUTS</span></span>

## <span data-ttu-id="65b3d-173">Note</span><span class="sxs-lookup"><span data-stu-id="65b3d-173">NOTES</span></span>

## <span data-ttu-id="65b3d-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65b3d-174">RELATED LINKS</span></span>

[<span data-ttu-id="65b3d-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="65b3d-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="65b3d-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="65b3d-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="65b3d-177">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="65b3d-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


