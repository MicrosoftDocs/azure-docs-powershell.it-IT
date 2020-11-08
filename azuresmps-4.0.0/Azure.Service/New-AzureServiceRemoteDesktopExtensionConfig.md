---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023853"
---
# <span data-ttu-id="94c53-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="94c53-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="94c53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94c53-102">SYNOPSIS</span></span>
<span data-ttu-id="94c53-103">Genera una configurazione dell'estensione desktop remoto per una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="94c53-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="94c53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94c53-104">SYNTAX</span></span>

### <span data-ttu-id="94c53-105">NewExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94c53-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="94c53-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="94c53-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="94c53-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94c53-107">DESCRIPTION</span></span>
<span data-ttu-id="94c53-108">Il cmdlet **New-AzureServiceRemoteDesktopExtensionConfig** genera una configurazione per un'estensione desktop remoto per una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="94c53-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="94c53-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94c53-109">EXAMPLES</span></span>

### <span data-ttu-id="94c53-110">Esempio 1: generazione di una configurazione di estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="94c53-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="94c53-111">Questo comando genera una configurazione dell'estensione desktop remoto per le credenziali specificate.</span><span class="sxs-lookup"><span data-stu-id="94c53-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="94c53-112">Esempio 2: generare una configurazione dell'estensione desktop remoto per un ruolo specificato</span><span class="sxs-lookup"><span data-stu-id="94c53-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="94c53-113">Questo comando genera una configurazione dell'estensione desktop remoto per le credenziali specificate e il ruolo WebRole01.</span><span class="sxs-lookup"><span data-stu-id="94c53-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="94c53-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94c53-114">PARAMETERS</span></span>

### <span data-ttu-id="94c53-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="94c53-115">-CertificateThumbprint</span></span>
<span data-ttu-id="94c53-116">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="94c53-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="94c53-117">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="94c53-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="94c53-118">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="94c53-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c53-119">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="94c53-119">-Credential</span></span>
<span data-ttu-id="94c53-120">Specifica le credenziali da abilitare per il desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="94c53-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="94c53-121">Le credenziali includono un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="94c53-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c53-122">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="94c53-122">-Expiration</span></span>
<span data-ttu-id="94c53-123">Specifica un oggetto **DateTime** che consente all'utente di specificare quando scade l'account utente.</span><span class="sxs-lookup"><span data-stu-id="94c53-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c53-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="94c53-124">-ExtensionId</span></span>
<span data-ttu-id="94c53-125">Specifica l'ID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="94c53-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c53-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="94c53-126">-InformationAction</span></span>
<span data-ttu-id="94c53-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="94c53-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="94c53-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94c53-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94c53-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="94c53-129">Continue</span></span>
- <span data-ttu-id="94c53-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="94c53-130">Ignore</span></span>
- <span data-ttu-id="94c53-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="94c53-131">Inquire</span></span>
- <span data-ttu-id="94c53-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="94c53-132">SilentlyContinue</span></span>
- <span data-ttu-id="94c53-133">Stop</span><span class="sxs-lookup"><span data-stu-id="94c53-133">Stop</span></span>
- <span data-ttu-id="94c53-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="94c53-134">Suspend</span></span>

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

### <span data-ttu-id="94c53-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="94c53-135">-InformationVariable</span></span>
<span data-ttu-id="94c53-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="94c53-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="94c53-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="94c53-137">-Profile</span></span>
<span data-ttu-id="94c53-138">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c53-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="94c53-139">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="94c53-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="94c53-140">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="94c53-140">-Role</span></span>
<span data-ttu-id="94c53-141">Specifica una matrice facoltativa di ruoli per cui specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="94c53-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="94c53-142">Se questo parametro non viene specificato, la configurazione desktop remoto viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="94c53-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="94c53-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="94c53-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="94c53-144">Specifica un algoritmo di hash dell'identificazione digitale usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="94c53-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="94c53-145">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="94c53-145">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="94c53-146">-Versione</span><span class="sxs-lookup"><span data-stu-id="94c53-146">-Version</span></span>
<span data-ttu-id="94c53-147">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="94c53-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c53-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="94c53-148">-X509Certificate</span></span>
<span data-ttu-id="94c53-149">Specifica un certificato X509 che, se specificato, verrà caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="94c53-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c53-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c53-150">CommonParameters</span></span>
<span data-ttu-id="94c53-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c53-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c53-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c53-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c53-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94c53-153">INPUTS</span></span>

## <span data-ttu-id="94c53-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94c53-154">OUTPUTS</span></span>

## <span data-ttu-id="94c53-155">Note</span><span class="sxs-lookup"><span data-stu-id="94c53-155">NOTES</span></span>

## <span data-ttu-id="94c53-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94c53-156">RELATED LINKS</span></span>

[<span data-ttu-id="94c53-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="94c53-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


