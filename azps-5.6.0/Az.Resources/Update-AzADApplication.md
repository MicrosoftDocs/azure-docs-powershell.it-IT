---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 329620701c4afb52bdebd145ef461c7d311c26a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997147"
---
# <span data-ttu-id="5e0a1-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5e0a1-101">Update-AzADApplication</span></span>

## <span data-ttu-id="5e0a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0a1-103">Aggiorna un'applicazione Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="5e0a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e0a1-104">SYNTAX</span></span>

### <span data-ttu-id="5e0a1-105">ApplicationObjectIdWithUpdateParamsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e0a1-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e0a1-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e0a1-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e0a1-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e0a1-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e0a1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e0a1-108">DESCRIPTION</span></span>
<span data-ttu-id="5e0a1-109">Aggiorna un'applicazione Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="5e0a1-110">Per aggiornare le credenziali associate all'applicazione, usare il cmdlet New-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="5e0a1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e0a1-111">EXAMPLES</span></span>

### <span data-ttu-id="5e0a1-112">Esempio 1 - Aggiornare il nome visualizzato di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="5e0a1-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="5e0a1-113">Aggiorna il nome visualizzato dell'applicazione il cui ID oggetto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' sarà "NomeVisualizzazioneNew".</span><span class="sxs-lookup"><span data-stu-id="5e0a1-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="5e0a1-114">Esempio 2 - Aggiornare tutte le proprietà di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="5e0a1-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="5e0a1-115">Aggiorna le proprietà di un'applicazione con ID oggetto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="5e0a1-116">Esempio 3 - Aggiornare il nome visualizzato di un'applicazione tramite piping</span><span class="sxs-lookup"><span data-stu-id="5e0a1-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="5e0a1-117">Ottiene l'applicazione con ID oggetto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' e pipe che al cmdlet Update-AzADApplication per aggiornare il nome visualizzato dell'applicazione in "NomeVisualizzazioneNew".</span><span class="sxs-lookup"><span data-stu-id="5e0a1-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="5e0a1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e0a1-118">PARAMETERS</span></span>

### <span data-ttu-id="5e0a1-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5e0a1-119">-ApplicationId</span></span>
<span data-ttu-id="5e0a1-120">ID applicazione dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="5e0a1-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="5e0a1-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="5e0a1-122">True se l'applicazione è condivisa con altri tenant; in caso contrario false.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="5e0a1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0a1-123">-DefaultProfile</span></span>
<span data-ttu-id="5e0a1-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e0a1-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e0a1-125">-DisplayName</span></span>
<span data-ttu-id="5e0a1-126">Nome visualizzato dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="5e0a1-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="5e0a1-127">-HomePage</span></span>
<span data-ttu-id="5e0a1-128">URL della home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="5e0a1-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="5e0a1-129">-IdentifierUri</span></span>
<span data-ttu-id="5e0a1-130">URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="5e0a1-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e0a1-131">-InputObject</span></span>
<span data-ttu-id="5e0a1-132">Oggetto che rappresenta l'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0a1-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5e0a1-133">-ObjectId</span></span>
<span data-ttu-id="5e0a1-134">ID oggetto dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0a1-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="5e0a1-135">-ReplyUrl</span></span>
<span data-ttu-id="5e0a1-136">Specifica gli URL a cui vengono inviati i token utente per l'accesso o gli URL di reindirizzamento a cui vengono inviati i codici di autorizzazione e i token di accesso di OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="5e0a1-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e0a1-137">-Confirm</span></span>
<span data-ttu-id="5e0a1-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e0a1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0a1-139">-WhatIf</span></span>
<span data-ttu-id="5e0a1-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0a1-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e0a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0a1-142">CommonParameters</span></span>
<span data-ttu-id="5e0a1-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0a1-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e0a1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0a1-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e0a1-145">INPUTS</span></span>

### <span data-ttu-id="5e0a1-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5e0a1-146">System.String</span></span>

### <span data-ttu-id="5e0a1-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5e0a1-147">System.Guid</span></span>

### <span data-ttu-id="5e0a1-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5e0a1-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="5e0a1-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5e0a1-149">System.String[]</span></span>

### <span data-ttu-id="5e0a1-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e0a1-150">System.Boolean</span></span>

## <span data-ttu-id="5e0a1-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e0a1-151">OUTPUTS</span></span>

### <span data-ttu-id="5e0a1-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5e0a1-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="5e0a1-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e0a1-153">NOTES</span></span>

## <span data-ttu-id="5e0a1-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e0a1-154">RELATED LINKS</span></span>
