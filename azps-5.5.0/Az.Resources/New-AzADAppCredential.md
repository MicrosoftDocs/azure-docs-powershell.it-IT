---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186447"
---
# <span data-ttu-id="9306b-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9306b-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="9306b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9306b-102">SYNOPSIS</span></span>
<span data-ttu-id="9306b-103">Aggiunge credenziali a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="9306b-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="9306b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9306b-104">SYNTAX</span></span>

### <span data-ttu-id="9306b-105">ApplicationObjectIdWithPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9306b-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9306b-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9306b-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9306b-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9306b-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9306b-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="9306b-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9306b-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="9306b-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9306b-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9306b-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9306b-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9306b-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9306b-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="9306b-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9306b-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9306b-113">DESCRIPTION</span></span>
<span data-ttu-id="9306b-114">Il New-AzADAppCredential cmdlet può essere usato per aggiungere nuove credenziali o per implementare le credenziali per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9306b-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="9306b-115">L'applicazione viene identificata fornendo l'ID oggetto applicazione o l'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="9306b-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="9306b-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9306b-116">EXAMPLES</span></span>

### <span data-ttu-id="9306b-117">Esempio 1 - Creare nuove credenziali dell'applicazione usando una password</span><span class="sxs-lookup"><span data-stu-id="9306b-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="9306b-118">All'applicazione esistente viene aggiunta una nuova password con ID oggetto '1f89cf81-0146-4f4e-beae-2007d0668416'.</span><span class="sxs-lookup"><span data-stu-id="9306b-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="9306b-119">Esempio 2 - Creare una nuova credenziali dell'applicazione usando un certificato</span><span class="sxs-lookup"><span data-stu-id="9306b-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="9306b-120">Il certificato X509 pubblico codificato base64 fornito ("myapp.cer") viene aggiunto all'applicazione esistente con ID applicazione '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="9306b-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="9306b-121">Esempio 3 - Creare nuove credenziali dell'applicazione tramite piping</span><span class="sxs-lookup"><span data-stu-id="9306b-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="9306b-122">Ottiene l'applicazione con ID oggetto '1f89cf81-0146-4f4e-beae-2007d0668416' e pipe che al New-AzADAppCredential per creare una nuova credenziali dell'applicazione con la password specificata.</span><span class="sxs-lookup"><span data-stu-id="9306b-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="9306b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9306b-123">PARAMETERS</span></span>

### <span data-ttu-id="9306b-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9306b-124">-ApplicationId</span></span>
<span data-ttu-id="9306b-125">ID applicazione dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="9306b-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="9306b-126">-ApplicationObject</span></span>
<span data-ttu-id="9306b-127">Oggetto applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="9306b-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="9306b-128">-CertValue</span></span>
<span data-ttu-id="9306b-129">Valore del tipo di credenziali "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="9306b-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="9306b-130">Rappresenta il certificato codificato base 64.</span><span class="sxs-lookup"><span data-stu-id="9306b-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9306b-131">-DefaultProfile</span></span>
<span data-ttu-id="9306b-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="9306b-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9306b-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9306b-133">-DisplayName</span></span>
<span data-ttu-id="9306b-134">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9306b-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9306b-135">-EndDate</span></span>
<span data-ttu-id="9306b-136">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9306b-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="9306b-137">Il valore predefinito per la data di fine è a un anno dalla data odierna.</span><span class="sxs-lookup"><span data-stu-id="9306b-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="9306b-138">Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="9306b-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9306b-139">-ObjectId</span></span>
<span data-ttu-id="9306b-140">ID oggetto dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="9306b-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-141">-Password</span><span class="sxs-lookup"><span data-stu-id="9306b-141">-Password</span></span>
<span data-ttu-id="9306b-142">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9306b-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9306b-143">-StartDate</span></span>
<span data-ttu-id="9306b-144">Data di inizio effettivo dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9306b-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="9306b-145">Il valore predefinito per la data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="9306b-145">The default start date value is today.</span></span> <span data-ttu-id="9306b-146">Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o dopo la data da cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="9306b-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9306b-147">-Confirm</span></span>
<span data-ttu-id="9306b-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9306b-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9306b-149">-WhatIf</span></span>
<span data-ttu-id="9306b-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9306b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9306b-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9306b-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9306b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9306b-152">CommonParameters</span></span>
<span data-ttu-id="9306b-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9306b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9306b-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9306b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9306b-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="9306b-155">INPUTS</span></span>

### <span data-ttu-id="9306b-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9306b-156">System.String</span></span>

### <span data-ttu-id="9306b-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9306b-157">System.Guid</span></span>

### <span data-ttu-id="9306b-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9306b-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="9306b-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="9306b-159">System.Security.SecureString</span></span>

### <span data-ttu-id="9306b-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="9306b-160">System.DateTime</span></span>

## <span data-ttu-id="9306b-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9306b-161">OUTPUTS</span></span>

### <span data-ttu-id="9306b-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9306b-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9306b-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="9306b-163">NOTES</span></span>

## <span data-ttu-id="9306b-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9306b-164">RELATED LINKS</span></span>

[<span data-ttu-id="9306b-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9306b-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="9306b-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9306b-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="9306b-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9306b-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

