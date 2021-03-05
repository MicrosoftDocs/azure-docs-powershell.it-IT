---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 93e2b62cf1261b20df1ea6c90d48caa1e1d88ec2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982190"
---
# <span data-ttu-id="8ba83-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8ba83-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="8ba83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba83-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba83-103">Rimuove le credenziali da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8ba83-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="8ba83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ba83-104">SYNTAX</span></span>

### <span data-ttu-id="8ba83-105">ApplicationObjectIdWithKeyIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ba83-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba83-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba83-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba83-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba83-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba83-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba83-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba83-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8ba83-109">DESCRIPTION</span></span>
<span data-ttu-id="8ba83-110">Il Remove-AzADAppCredential cmdlet può essere usato per rimuovere una chiave delle credenziali da un'applicazione in caso di compromissione o come parte della scadenza del rollover della chiave delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="8ba83-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="8ba83-111">L'applicazione viene identificata fornendo l'ID oggetto o l'AppId.</span><span class="sxs-lookup"><span data-stu-id="8ba83-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="8ba83-112">Le credenziali da rimuovere sono identificate dal relativo ID chiave.</span><span class="sxs-lookup"><span data-stu-id="8ba83-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="8ba83-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ba83-113">EXAMPLES</span></span>

### <span data-ttu-id="8ba83-114">Esempio 1: Rimuovere credenziali specifiche da un'applicazione</span><span class="sxs-lookup"><span data-stu-id="8ba83-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="8ba83-115">Rimuove le credenziali con ID chiave '9044423a-60a3-45ac-9ab1-09534157ebb' dall'applicazione con ID oggetto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="8ba83-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="8ba83-116">Esempio 2: Rimuovere tutte le credenziali da un'applicazione</span><span class="sxs-lookup"><span data-stu-id="8ba83-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="8ba83-117">Rimuove tutte le credenziali dall'applicazione con ID applicazione '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="8ba83-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="8ba83-118">Esempio 3: Rimuovere tutte le credenziali tramite piping</span><span class="sxs-lookup"><span data-stu-id="8ba83-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="8ba83-119">Ottiene l'applicazione con ID oggetto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' e pipe al cmdlet di Remove-AzADAppCredential e rimuove tutte le credenziali dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8ba83-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="8ba83-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ba83-120">PARAMETERS</span></span>

### <span data-ttu-id="8ba83-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8ba83-121">-ApplicationId</span></span>
<span data-ttu-id="8ba83-122">ID dell'applicazione da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="8ba83-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8ba83-123">-ApplicationObject</span></span>
<span data-ttu-id="8ba83-124">Oggetto applicazione da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="8ba83-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba83-125">-DefaultProfile</span></span>
<span data-ttu-id="8ba83-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8ba83-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ba83-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8ba83-127">-DisplayName</span></span>
<span data-ttu-id="8ba83-128">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8ba83-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8ba83-129">-Force</span></span>
<span data-ttu-id="8ba83-130">Passare all'eliminazione delle credenziali senza conferma.</span><span class="sxs-lookup"><span data-stu-id="8ba83-130">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="8ba83-131">-KeyId</span></span>
<span data-ttu-id="8ba83-132">Specifica la chiave delle credenziali da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8ba83-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="8ba83-133">Gli ID chiave per l'applicazione possono essere ottenuti con il cmdlet Get-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="8ba83-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8ba83-134">-ObjectId</span></span>
<span data-ttu-id="8ba83-135">ID oggetto dell'applicazione da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="8ba83-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ba83-136">-PassThru</span></span>
<span data-ttu-id="8ba83-137">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8ba83-137">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba83-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ba83-138">-Confirm</span></span>
<span data-ttu-id="8ba83-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba83-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba83-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba83-140">-WhatIf</span></span>
<span data-ttu-id="8ba83-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ba83-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba83-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ba83-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba83-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba83-143">CommonParameters</span></span>
<span data-ttu-id="8ba83-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba83-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba83-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8ba83-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba83-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="8ba83-146">INPUTS</span></span>

### <span data-ttu-id="8ba83-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8ba83-147">System.String</span></span>

### <span data-ttu-id="8ba83-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8ba83-148">System.Guid</span></span>

### <span data-ttu-id="8ba83-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8ba83-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8ba83-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ba83-150">OUTPUTS</span></span>

### <span data-ttu-id="8ba83-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ba83-151">System.Boolean</span></span>

## <span data-ttu-id="8ba83-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="8ba83-152">NOTES</span></span>

## <span data-ttu-id="8ba83-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ba83-153">RELATED LINKS</span></span>

[<span data-ttu-id="8ba83-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8ba83-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="8ba83-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8ba83-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8ba83-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8ba83-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
