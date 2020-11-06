---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADApplication.md
ms.openlocfilehash: c0d1b1debfa7d360e821ffc56a8b2e6fa821c6e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520853"
---
# <span data-ttu-id="36664-101">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="36664-101">Update-AzureRmADApplication</span></span>

## <span data-ttu-id="36664-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36664-102">SYNOPSIS</span></span>
<span data-ttu-id="36664-103">Aggiorna un'applicazione di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="36664-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36664-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36664-104">SYNTAX</span></span>

### <span data-ttu-id="36664-105">ApplicationObjectIdWithUpdateParamsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36664-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzureRmADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36664-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="36664-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36664-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="36664-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36664-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36664-108">DESCRIPTION</span></span>
<span data-ttu-id="36664-109">Aggiorna un'applicazione di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="36664-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="36664-110">Per aggiornare le credenziali associate a questa applicazione, usare il cmdlet New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="36664-110">To update the credentials associated with this application, please use the New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="36664-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36664-111">EXAMPLES</span></span>

### <span data-ttu-id="36664-112">Esempio 1-aggiornare il nome visualizzato di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="36664-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="36664-113">Aggiorna il nome visualizzato dell'applicazione con l'ID oggetto "fb7b3405-CA44-4B5B-8584-12392f5d96d7" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="36664-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="36664-114">Esempio 2-aggiornare tutte le proprietà di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="36664-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="36664-115">Aggiorna le proprietà di un'applicazione con l'ID oggetto "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="36664-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="36664-116">Esempio 3-aggiornare il nome visualizzato di un'applicazione tramite piping</span><span class="sxs-lookup"><span data-stu-id="36664-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzureRmADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="36664-117">Ottiene l'applicazione con l'ID oggetto "fb7b3405-CA44-4B5B-8584-12392f5d96d7" e le pipe al cmdlet Update-AzureRmADApplication per aggiornare il nome visualizzato dell'applicazione in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="36664-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzureRmADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="36664-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36664-118">PARAMETERS</span></span>

### <span data-ttu-id="36664-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="36664-119">-ApplicationId</span></span>
<span data-ttu-id="36664-120">ID applicazione dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="36664-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="36664-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="36664-122">True se l'applicazione è condivisa con altri tenant; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="36664-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36664-123">-DefaultProfile</span></span>
<span data-ttu-id="36664-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36664-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36664-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="36664-125">-DisplayName</span></span>
<span data-ttu-id="36664-126">Nome visualizzato per l'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="36664-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-127">-Home page</span><span class="sxs-lookup"><span data-stu-id="36664-127">-HomePage</span></span>
<span data-ttu-id="36664-128">URL della Home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="36664-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="36664-129">-IdentifierUri</span></span>
<span data-ttu-id="36664-130">URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="36664-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36664-131">-InputObject</span></span>
<span data-ttu-id="36664-132">Oggetto che rappresenta l'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="36664-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="36664-133">-ObjectId</span></span>
<span data-ttu-id="36664-134">ID oggetto dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="36664-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="36664-135">-ReplyUrl</span></span>
<span data-ttu-id="36664-136">Specifica gli URL a cui vengono inviati i token utente per l'accesso oppure gli URI di reindirizzamento in cui vengono inviati i codici di autorizzazione OAuth 2,0 e i token di accesso.</span><span class="sxs-lookup"><span data-stu-id="36664-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36664-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36664-137">-Confirm</span></span>
<span data-ttu-id="36664-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36664-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36664-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36664-139">-WhatIf</span></span>
<span data-ttu-id="36664-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36664-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36664-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36664-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36664-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36664-142">CommonParameters</span></span>
<span data-ttu-id="36664-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36664-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36664-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36664-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36664-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36664-145">INPUTS</span></span>

### <span data-ttu-id="36664-146">System. Guid</span><span class="sxs-lookup"><span data-stu-id="36664-146">System.Guid</span></span>

### <span data-ttu-id="36664-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="36664-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="36664-148">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36664-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="36664-149">System. String</span><span class="sxs-lookup"><span data-stu-id="36664-149">System.String</span></span>

### <span data-ttu-id="36664-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="36664-150">System.String[]</span></span>

### <span data-ttu-id="36664-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36664-151">System.Boolean</span></span>

## <span data-ttu-id="36664-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36664-152">OUTPUTS</span></span>

### <span data-ttu-id="36664-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="36664-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="36664-154">Note</span><span class="sxs-lookup"><span data-stu-id="36664-154">NOTES</span></span>

## <span data-ttu-id="36664-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36664-155">RELATED LINKS</span></span>
