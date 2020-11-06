---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 15b3e3fd90a7bacf87062bc12269ca2853276370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521545"
---
# <span data-ttu-id="fef56-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fef56-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="fef56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fef56-102">SYNOPSIS</span></span>
<span data-ttu-id="fef56-103">Aggiunge una credenziale a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="fef56-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fef56-104">SYNTAX</span></span>

### <span data-ttu-id="fef56-105">ApplicationObjectIdWithPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fef56-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fef56-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fef56-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fef56-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fef56-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fef56-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fef56-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef56-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fef56-109">DESCRIPTION</span></span>
<span data-ttu-id="fef56-110">Il cmdlet New-AzureRmADAppCredential può essere usato per aggiungere una nuova credenziale o per eseguire il rollforward delle credenziali per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fef56-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="fef56-111">L'applicazione viene identificata fornendo l'ID oggetto applicazione o l'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="fef56-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="fef56-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fef56-112">EXAMPLES</span></span>

### <span data-ttu-id="fef56-113">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fef56-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password P@ssw0rd!
```

<span data-ttu-id="fef56-114">Viene aggiunta una nuova credenziale password a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="fef56-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="fef56-115">In questo esempio, il valore della password fornito viene aggiunto all'applicazione usando l'ID oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="fef56-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="fef56-116">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fef56-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="fef56-117">Una nuova credenziale chiave viene aggiunta a un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="fef56-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="fef56-118">In questo esempio, il certificato di X509 pubblico con codifica Base64 fornito ("MyApp. cer") viene aggiunto all'applicazione usando applicationId.</span><span class="sxs-lookup"><span data-stu-id="fef56-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="fef56-119">--------------------------Esempio 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="fef56-119">--------------------------  Example 3  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="fef56-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fef56-120">PARAMETERS</span></span>

### <span data-ttu-id="fef56-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fef56-121">-ApplicationId</span></span>
<span data-ttu-id="fef56-122">ID dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="fef56-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef56-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="fef56-123">-CertValue</span></span>
<span data-ttu-id="fef56-124">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="fef56-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="fef56-125">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="fef56-125">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="fef56-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fef56-126">-EndDate</span></span>
<span data-ttu-id="fef56-127">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fef56-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="fef56-128">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="fef56-128">The default end date value is one year from today.</span></span> <span data-ttu-id="fef56-129">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="fef56-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="fef56-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fef56-130">-ObjectId</span></span>
<span data-ttu-id="fef56-131">ID oggetto dell'applicazione a cui aggiungere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="fef56-131">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="fef56-132">-Password</span><span class="sxs-lookup"><span data-stu-id="fef56-132">-Password</span></span>
<span data-ttu-id="fef56-133">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fef56-133">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef56-134">-StartDate</span><span class="sxs-lookup"><span data-stu-id="fef56-134">-StartDate</span></span>
<span data-ttu-id="fef56-135">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fef56-135">The effective start date of the credential usage.</span></span>
<span data-ttu-id="fef56-136">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="fef56-136">The default start date value is today.</span></span>
<span data-ttu-id="fef56-137">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="fef56-137">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="fef56-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fef56-138">-Confirm</span></span>
<span data-ttu-id="fef56-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fef56-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fef56-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef56-140">-WhatIf</span></span>
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

### <span data-ttu-id="fef56-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef56-141">-DefaultProfile</span></span>
<span data-ttu-id="fef56-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fef56-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fef56-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef56-143">CommonParameters</span></span>
<span data-ttu-id="fef56-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef56-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef56-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef56-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef56-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fef56-146">INPUTS</span></span>

## <span data-ttu-id="fef56-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fef56-147">OUTPUTS</span></span>

### <span data-ttu-id="fef56-148">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="fef56-148">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="fef56-149">Note</span><span class="sxs-lookup"><span data-stu-id="fef56-149">NOTES</span></span>

## <span data-ttu-id="fef56-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fef56-150">RELATED LINKS</span></span>

[<span data-ttu-id="fef56-151">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fef56-151">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="fef56-152">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fef56-152">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="fef56-153">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="fef56-153">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

