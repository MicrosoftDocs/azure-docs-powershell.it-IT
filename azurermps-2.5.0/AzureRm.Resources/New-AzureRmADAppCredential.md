---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
ms.openlocfilehash: a3571b737e07247a21364ed0b789c583892500c5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866636"
---
# <span data-ttu-id="c4c95-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4c95-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="c4c95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4c95-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c95-103">Aggiunge una credenziale a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c4c95-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4c95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4c95-104">SYNTAX</span></span>

### <span data-ttu-id="c4c95-105">ApplicationObjectIdWithPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4c95-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c95-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c95-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c95-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c95-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c95-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c95-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c95-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c95-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c95-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c95-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c95-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c95-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c95-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4c95-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4c95-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4c95-113">DESCRIPTION</span></span>
<span data-ttu-id="c4c95-114">Il cmdlet New-AzureRmADAppCredential può essere usato per aggiungere una nuova credenziale o per eseguire il rollforward delle credenziali per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c4c95-114">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="c4c95-115">L'applicazione viene identificata fornendo l'ID oggetto applicazione o l'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="c4c95-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="c4c95-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4c95-116">EXAMPLES</span></span>

### <span data-ttu-id="c4c95-117">Esempio 1-creare una nuova credenziale applicativa usando una password</span><span class="sxs-lookup"><span data-stu-id="c4c95-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="c4c95-118">Viene aggiunta una nuova credenziale password al appplication esistente con l'ID oggetto "1f89cf81-0146-4f4e-BEAE-2007d0668416".</span><span class="sxs-lookup"><span data-stu-id="c4c95-118">A new password credential is added to the existing appplication with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="c4c95-119">Esempio 2: creare una nuova credenziale applicativa usando un certificato</span><span class="sxs-lookup"><span data-stu-id="c4c95-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="c4c95-120">Il certificato X509 pubblico con codifica Base64 fornito ("MyApp. cer") viene aggiunto all'applicazione esistente con l'ID applicazione "4589cd6b-3D79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="c4c95-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="c4c95-121">Esempio 3-creare una nuova credenziale applicativa tramite piping</span><span class="sxs-lookup"><span data-stu-id="c4c95-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzureRmADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzureRmADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="c4c95-122">Ottiene l'applicazione con l'ID oggetto "1f89cf81-0146-4f4e-BEAE-2007d0668416" e convoglia la New-AzureRmADAppCredential per creare una nuova credenziale dell'applicazione con la password specificata.</span><span class="sxs-lookup"><span data-stu-id="c4c95-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzureRmADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="c4c95-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4c95-123">PARAMETERS</span></span>

### <span data-ttu-id="c4c95-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c4c95-124">-ApplicationId</span></span>
<span data-ttu-id="c4c95-125">ID applicazione dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="c4c95-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="c4c95-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c4c95-126">-ApplicationObject</span></span>
<span data-ttu-id="c4c95-127">L'oggetto Application per cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="c4c95-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c95-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="c4c95-128">-CertValue</span></span>
<span data-ttu-id="c4c95-129">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="c4c95-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="c4c95-130">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="c4c95-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="c4c95-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c95-131">-DefaultProfile</span></span>
<span data-ttu-id="c4c95-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c4c95-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c95-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c4c95-133">-DisplayName</span></span>
<span data-ttu-id="c4c95-134">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c4c95-134">The display name of the application.</span></span>

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

### <span data-ttu-id="c4c95-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c4c95-135">-EndDate</span></span>
<span data-ttu-id="c4c95-136">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c4c95-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="c4c95-137">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="c4c95-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="c4c95-138">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="c4c95-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="c4c95-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c4c95-139">-ObjectId</span></span>
<span data-ttu-id="c4c95-140">ID oggetto dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="c4c95-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c95-141">-Password</span><span class="sxs-lookup"><span data-stu-id="c4c95-141">-Password</span></span>
<span data-ttu-id="c4c95-142">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c4c95-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="c4c95-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c4c95-143">-StartDate</span></span>
<span data-ttu-id="c4c95-144">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c4c95-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="c4c95-145">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="c4c95-145">The default start date value is today.</span></span> <span data-ttu-id="c4c95-146">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="c4c95-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="c4c95-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4c95-147">-Confirm</span></span>
<span data-ttu-id="c4c95-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c95-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c95-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c95-149">-WhatIf</span></span>
<span data-ttu-id="c4c95-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4c95-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c95-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4c95-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c95-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c95-152">CommonParameters</span></span>
<span data-ttu-id="c4c95-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c95-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c95-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c95-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c95-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4c95-155">INPUTS</span></span>

### <span data-ttu-id="c4c95-156">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c4c95-156">System.Guid</span></span>

### <span data-ttu-id="c4c95-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c4c95-157">System.String</span></span>

### <span data-ttu-id="c4c95-158">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c4c95-158">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="c4c95-159">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4c95-159">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="c4c95-160">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c4c95-160">System.Security.SecureString</span></span>

### <span data-ttu-id="c4c95-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c4c95-161">System.DateTime</span></span>

## <span data-ttu-id="c4c95-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4c95-162">OUTPUTS</span></span>

### <span data-ttu-id="c4c95-163">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="c4c95-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="c4c95-164">Note</span><span class="sxs-lookup"><span data-stu-id="c4c95-164">NOTES</span></span>

## <span data-ttu-id="c4c95-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4c95-165">RELATED LINKS</span></span>

[<span data-ttu-id="c4c95-166">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4c95-166">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="c4c95-167">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4c95-167">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="c4c95-168">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c4c95-168">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

