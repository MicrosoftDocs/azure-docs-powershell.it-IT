---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 5c47e707c3421c6efc1998e55897f6bb9be8fa65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854817"
---
# <span data-ttu-id="7e251-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e251-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="7e251-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e251-102">SYNOPSIS</span></span>
<span data-ttu-id="7e251-103">Rimuove una credenziale da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e251-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="7e251-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e251-104">SYNTAX</span></span>

### <span data-ttu-id="7e251-105">ApplicationObjectIdWithKeyIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e251-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e251-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e251-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e251-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e251-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e251-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e251-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e251-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e251-109">DESCRIPTION</span></span>
<span data-ttu-id="7e251-110">Il cmdlet Remove-AzADAppCredential può essere usato per rimuovere una chiave di credenziale da un'applicazione in caso di compromissione o come parte della scadenza del rollover della chiave di credenziale.</span><span class="sxs-lookup"><span data-stu-id="7e251-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7e251-111">L'applicazione viene identificata fornendo l'ID oggetto o l'AppId.</span><span class="sxs-lookup"><span data-stu-id="7e251-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="7e251-112">La credenziale da rimuovere viene identificata dall'ID chiave.</span><span class="sxs-lookup"><span data-stu-id="7e251-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="7e251-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e251-113">EXAMPLES</span></span>

### <span data-ttu-id="7e251-114">Esempio 1-rimuovere una specifica credenziale da un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7e251-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7e251-115">Rimuove le credenziali con l'ID chiave ' 9044423a-60A3-45AC-9ab1-09534157ebb ' dall'applicazione con l'ID oggetto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="7e251-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="7e251-116">Esempio 2-Rimuovere tutte le credenziali da un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7e251-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="7e251-117">Rimuove tutte le credenziali dall'applicazione con l'ID applicazione ' 4589cd6b-3D79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="7e251-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="7e251-118">Esempio 3-rimuovere tutte le credenziali tramite piping</span><span class="sxs-lookup"><span data-stu-id="7e251-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="7e251-119">Ottiene l'applicazione con l'ID oggetto "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" e le pipe al cmdlet Remove-AzADAppCredential e rimuove tutte le credenziali dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e251-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="7e251-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e251-120">PARAMETERS</span></span>

### <span data-ttu-id="7e251-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7e251-121">-ApplicationId</span></span>
<span data-ttu-id="7e251-122">ID dell'applicazione per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7e251-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="7e251-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7e251-123">-ApplicationObject</span></span>
<span data-ttu-id="7e251-124">Oggetto Application per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7e251-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="7e251-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e251-125">-DefaultProfile</span></span>
<span data-ttu-id="7e251-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7e251-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e251-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7e251-127">-DisplayName</span></span>
<span data-ttu-id="7e251-128">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e251-128">The display name of the application.</span></span>

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

### <span data-ttu-id="7e251-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7e251-129">-Force</span></span>
<span data-ttu-id="7e251-130">Passare a eliminare le credenziali senza conferma.</span><span class="sxs-lookup"><span data-stu-id="7e251-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="7e251-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7e251-131">-KeyId</span></span>
<span data-ttu-id="7e251-132">Specifica la chiave delle credenziali da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7e251-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7e251-133">Gli ID chiave per l'applicazione possono essere ottenuti usando il cmdlet Get-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="7e251-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="7e251-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7e251-134">-ObjectId</span></span>
<span data-ttu-id="7e251-135">ID oggetto dell'applicazione per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7e251-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="7e251-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e251-136">-PassThru</span></span>
<span data-ttu-id="7e251-137">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="7e251-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7e251-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e251-138">-Confirm</span></span>
<span data-ttu-id="7e251-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e251-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e251-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e251-140">-WhatIf</span></span>
<span data-ttu-id="7e251-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e251-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e251-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e251-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e251-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e251-143">CommonParameters</span></span>
<span data-ttu-id="7e251-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e251-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e251-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e251-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e251-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e251-146">INPUTS</span></span>

### <span data-ttu-id="7e251-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7e251-147">System.String</span></span>

### <span data-ttu-id="7e251-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7e251-148">System.Guid</span></span>

### <span data-ttu-id="7e251-149">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7e251-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7e251-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e251-150">OUTPUTS</span></span>

### <span data-ttu-id="7e251-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e251-151">System.Boolean</span></span>

## <span data-ttu-id="7e251-152">Note</span><span class="sxs-lookup"><span data-stu-id="7e251-152">NOTES</span></span>

## <span data-ttu-id="7e251-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e251-153">RELATED LINKS</span></span>

[<span data-ttu-id="7e251-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e251-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="7e251-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e251-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="7e251-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7e251-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
