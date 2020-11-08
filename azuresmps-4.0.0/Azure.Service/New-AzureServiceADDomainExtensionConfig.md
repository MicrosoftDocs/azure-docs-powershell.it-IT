---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023855"
---
# <span data-ttu-id="7f488-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="7f488-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="7f488-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f488-102">SYNOPSIS</span></span>
<span data-ttu-id="7f488-103">Genera la configurazione per l'estensione del dominio Active Directory per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="7f488-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="7f488-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f488-104">SYNTAX</span></span>

### <span data-ttu-id="7f488-105">JoinDomainUsingEnumOptions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f488-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f488-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="7f488-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f488-107">Workgroup</span><span class="sxs-lookup"><span data-stu-id="7f488-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f488-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f488-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f488-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f488-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f488-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f488-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f488-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f488-111">DESCRIPTION</span></span>
<span data-ttu-id="7f488-112">Il cmdlet **New-AzureServiceADDomainExtensionConfig** genera la configurazione per l'estensione del dominio Active Directory (ad) per i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="7f488-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="7f488-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f488-113">EXAMPLES</span></span>

### <span data-ttu-id="7f488-114">Esempio 1: specificare una configurazione del dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="7f488-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="7f488-115">Questo comando genera una configurazione per l'estensione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f488-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="7f488-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f488-116">PARAMETERS</span></span>

### <span data-ttu-id="7f488-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f488-117">-CertificateThumbprint</span></span>
<span data-ttu-id="7f488-118">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="7f488-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="7f488-119">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="7f488-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="7f488-120">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="7f488-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-121">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="7f488-121">-Credential</span></span>
<span data-ttu-id="7f488-122">Specifica le credenziali da usare per partecipare al dominio di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f488-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="7f488-123">Le credenziali includono un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="7f488-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-124">-DomainName</span><span class="sxs-lookup"><span data-stu-id="7f488-124">-DomainName</span></span>
<span data-ttu-id="7f488-125">Specifica il nome di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f488-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="7f488-126">-ExtensionId</span></span>
<span data-ttu-id="7f488-127">Specifica l'ID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7f488-127">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7f488-128">-InformationAction</span></span>
<span data-ttu-id="7f488-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7f488-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7f488-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f488-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f488-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="7f488-131">Continue</span></span>
- <span data-ttu-id="7f488-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="7f488-132">Ignore</span></span>
- <span data-ttu-id="7f488-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7f488-133">Inquire</span></span>
- <span data-ttu-id="7f488-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7f488-134">SilentlyContinue</span></span>
- <span data-ttu-id="7f488-135">Stop</span><span class="sxs-lookup"><span data-stu-id="7f488-135">Stop</span></span>
- <span data-ttu-id="7f488-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7f488-136">Suspend</span></span>

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

### <span data-ttu-id="7f488-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7f488-137">-InformationVariable</span></span>
<span data-ttu-id="7f488-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f488-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7f488-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="7f488-139">-JoinOption</span></span>
<span data-ttu-id="7f488-140">Specifica l'enumerazione dell'opzione join.</span><span class="sxs-lookup"><span data-stu-id="7f488-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-141">-Opzioni</span><span class="sxs-lookup"><span data-stu-id="7f488-141">-Options</span></span>
<span data-ttu-id="7f488-142">Specifica l'opzione Unisci interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="7f488-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="7f488-143">-OUPath</span></span>
<span data-ttu-id="7f488-144">Specifica il percorso dell'unità organizzativa per l'operazione di partecipazione al dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f488-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-145">-Profile</span><span class="sxs-lookup"><span data-stu-id="7f488-145">-Profile</span></span>
<span data-ttu-id="7f488-146">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f488-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f488-147">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7f488-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f488-148">-Riavviare</span><span class="sxs-lookup"><span data-stu-id="7f488-148">-Restart</span></span>
<span data-ttu-id="7f488-149">Specifica se riavviare il computer se l'operazione di join riesce.</span><span class="sxs-lookup"><span data-stu-id="7f488-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-150">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="7f488-150">-Role</span></span>
<span data-ttu-id="7f488-151">Specifica una matrice facoltativa di ruoli per specificare la configurazione desktop remoto per la configurazione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f488-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="7f488-152">Se non specifichi questo parametro, la configurazione del dominio Active Directory viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="7f488-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7f488-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="7f488-154">Specifica un algoritmo di hash dell'identificazione digitale usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="7f488-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="7f488-155">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="7f488-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="7f488-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="7f488-157">Specifica le credenziali (nome utente e password) per la dispartecipazione al dominio di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f488-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-158">-Versione</span><span class="sxs-lookup"><span data-stu-id="7f488-158">-Version</span></span>
<span data-ttu-id="7f488-159">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7f488-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-160">-Workgroup</span><span class="sxs-lookup"><span data-stu-id="7f488-160">-WorkgroupName</span></span>
<span data-ttu-id="7f488-161">Specifica il nome del gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7f488-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="7f488-162">-X509Certificate</span></span>
<span data-ttu-id="7f488-163">Specifica un certificato X. 509 caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7f488-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f488-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f488-164">CommonParameters</span></span>
<span data-ttu-id="7f488-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f488-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f488-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f488-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f488-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f488-167">INPUTS</span></span>

## <span data-ttu-id="7f488-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f488-168">OUTPUTS</span></span>

## <span data-ttu-id="7f488-169">Note</span><span class="sxs-lookup"><span data-stu-id="7f488-169">NOTES</span></span>

## <span data-ttu-id="7f488-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f488-170">RELATED LINKS</span></span>

[<span data-ttu-id="7f488-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7f488-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="7f488-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7f488-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


