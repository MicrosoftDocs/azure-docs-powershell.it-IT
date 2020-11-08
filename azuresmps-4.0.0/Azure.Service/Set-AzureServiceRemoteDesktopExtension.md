---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023771"
---
# <span data-ttu-id="bcedc-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="bcedc-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="bcedc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcedc-102">SYNOPSIS</span></span>
<span data-ttu-id="bcedc-103">Abilita l'estensione desktop remoto in ruoli o ruoli specifici in un servizio distribuito o in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bcedc-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="bcedc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcedc-104">SYNTAX</span></span>

### <span data-ttu-id="bcedc-105">Seextension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcedc-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bcedc-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="bcedc-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bcedc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcedc-107">DESCRIPTION</span></span>
<span data-ttu-id="bcedc-108">Il cmdlet **set-AzureServiceRemoteDesktopExtension** Abilita l'estensione desktop remoto nei ruoli specificati o in tutti i ruoli in un servizio distribuito o alla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bcedc-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="bcedc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcedc-109">EXAMPLES</span></span>

### <span data-ttu-id="bcedc-110">Esempio 1: abilitare l'estensione desktop remoto</span><span class="sxs-lookup"><span data-stu-id="bcedc-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="bcedc-111">Questo comando Abilita l'estensione desktop remoto per il servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="bcedc-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="bcedc-112">Esempio 2: abilitare l'estensione desktop remoto per un ruolo specificato</span><span class="sxs-lookup"><span data-stu-id="bcedc-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="bcedc-113">Questo comando Abilita l'estensione desktop remoto per il servizio e il ruolo specificati.</span><span class="sxs-lookup"><span data-stu-id="bcedc-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="bcedc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcedc-114">PARAMETERS</span></span>

### <span data-ttu-id="bcedc-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="bcedc-115">-CertificateThumbprint</span></span>
<span data-ttu-id="bcedc-116">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="bcedc-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="bcedc-117">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="bcedc-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="bcedc-118">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="bcedc-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcedc-119">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="bcedc-119">-Credential</span></span>
<span data-ttu-id="bcedc-120">Specifica le credenziali da abilitare per il desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bcedc-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="bcedc-121">Le credenziali includono un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="bcedc-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcedc-122">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="bcedc-122">-Expiration</span></span>
<span data-ttu-id="bcedc-123">Specifica un oggetto data/ora che consente all'utente di specificare quando scade l'account utente.</span><span class="sxs-lookup"><span data-stu-id="bcedc-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcedc-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="bcedc-124">-ExtensionId</span></span>
<span data-ttu-id="bcedc-125">Specifica l'ID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="bcedc-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcedc-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bcedc-126">-InformationAction</span></span>
<span data-ttu-id="bcedc-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="bcedc-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bcedc-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bcedc-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bcedc-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="bcedc-129">Continue</span></span>
- <span data-ttu-id="bcedc-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="bcedc-130">Ignore</span></span>
- <span data-ttu-id="bcedc-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="bcedc-131">Inquire</span></span>
- <span data-ttu-id="bcedc-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bcedc-132">SilentlyContinue</span></span>
- <span data-ttu-id="bcedc-133">Stop</span><span class="sxs-lookup"><span data-stu-id="bcedc-133">Stop</span></span>
- <span data-ttu-id="bcedc-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="bcedc-134">Suspend</span></span>

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

### <span data-ttu-id="bcedc-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bcedc-135">-InformationVariable</span></span>
<span data-ttu-id="bcedc-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="bcedc-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bcedc-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="bcedc-137">-Profile</span></span>
<span data-ttu-id="bcedc-138">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcedc-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bcedc-139">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bcedc-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bcedc-140">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="bcedc-140">-Role</span></span>
<span data-ttu-id="bcedc-141">Specifica una matrice facoltativa di ruoli per cui specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bcedc-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="bcedc-142">Se questo parametro non viene specificato, la configurazione desktop remoto viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="bcedc-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="bcedc-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bcedc-143">-ServiceName</span></span>
<span data-ttu-id="bcedc-144">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bcedc-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="bcedc-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="bcedc-145">-Slot</span></span>
<span data-ttu-id="bcedc-146">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="bcedc-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="bcedc-147">I valori accettabili per questo parametro sono: produzione, staging.</span><span class="sxs-lookup"><span data-stu-id="bcedc-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="bcedc-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="bcedc-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="bcedc-149">Specifica un algoritmo di hash dell'identificazione digitale usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="bcedc-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="bcedc-150">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="bcedc-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="bcedc-151">-Versione</span><span class="sxs-lookup"><span data-stu-id="bcedc-151">-Version</span></span>
<span data-ttu-id="bcedc-152">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="bcedc-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcedc-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="bcedc-153">-X509Certificate</span></span>
<span data-ttu-id="bcedc-154">Specifica un certificato X509 caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="bcedc-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcedc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcedc-155">CommonParameters</span></span>
<span data-ttu-id="bcedc-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcedc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcedc-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcedc-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcedc-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcedc-158">INPUTS</span></span>

## <span data-ttu-id="bcedc-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcedc-159">OUTPUTS</span></span>

## <span data-ttu-id="bcedc-160">Note</span><span class="sxs-lookup"><span data-stu-id="bcedc-160">NOTES</span></span>

## <span data-ttu-id="bcedc-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcedc-161">RELATED LINKS</span></span>

[<span data-ttu-id="bcedc-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="bcedc-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


