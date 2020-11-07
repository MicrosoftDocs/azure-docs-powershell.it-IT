---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
ms.openlocfilehash: 0e442687604b99249f7e64a1c6d1fd4db91c38b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866798"
---
# <span data-ttu-id="4e916-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4e916-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="4e916-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e916-102">SYNOPSIS</span></span>
<span data-ttu-id="4e916-103">Rimuove una credenziale da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e916-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e916-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e916-104">SYNTAX</span></span>

### <span data-ttu-id="4e916-105">ApplicationObjectIdWithKeyIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e916-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e916-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e916-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e916-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e916-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e916-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e916-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e916-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e916-109">DESCRIPTION</span></span>
<span data-ttu-id="4e916-110">Il cmdlet Remove-AzureRmADAppCredential può essere usato per rimuovere una chiave di credenziale da un'applicazione in caso di compromissione o come parte della scadenza del rollover della chiave di credenziale.</span><span class="sxs-lookup"><span data-stu-id="4e916-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="4e916-111">L'applicazione viene identificata fornendo l'ID oggetto o l'AppId.</span><span class="sxs-lookup"><span data-stu-id="4e916-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="4e916-112">La credenziale da rimuovere viene identificata dall'ID chiave.</span><span class="sxs-lookup"><span data-stu-id="4e916-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="4e916-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e916-113">EXAMPLES</span></span>

### <span data-ttu-id="4e916-114">Esempio 1-rimuovere una specifica credenziale da un'applicazione</span><span class="sxs-lookup"><span data-stu-id="4e916-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="4e916-115">Rimuove le credenziali con l'ID chiave ' 9044423a-60A3-45AC-9ab1-09534157ebb ' dall'applicazione con l'ID oggetto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="4e916-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="4e916-116">Esempio 2-Rimuovere tutte le credenziali da un'applicazione</span><span class="sxs-lookup"><span data-stu-id="4e916-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="4e916-117">Rimuove tutte le credenziali dall'applicazione con l'ID applicazione ' 4589cd6b-3D79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="4e916-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="4e916-118">Esempio 3-rimuovere tutte le credenziali tramite piping</span><span class="sxs-lookup"><span data-stu-id="4e916-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

<span data-ttu-id="4e916-119">Ottiene l'applicazione con l'ID oggetto "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" e le pipe al cmdlet Remove-AzureRmADAppCredential e rimuove tutte le credenziali dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e916-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="4e916-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e916-120">PARAMETERS</span></span>

### <span data-ttu-id="4e916-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4e916-121">-ApplicationId</span></span>
<span data-ttu-id="4e916-122">ID dell'applicazione per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="4e916-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="4e916-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="4e916-123">-ApplicationObject</span></span>
<span data-ttu-id="4e916-124">Oggetto Application per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="4e916-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e916-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e916-125">-DefaultProfile</span></span>
<span data-ttu-id="4e916-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4e916-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e916-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4e916-127">-DisplayName</span></span>
<span data-ttu-id="4e916-128">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e916-128">The display name of the application.</span></span>

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

### <span data-ttu-id="4e916-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4e916-129">-Force</span></span>
<span data-ttu-id="4e916-130">Passare a eliminare le credenziali senza conferma.</span><span class="sxs-lookup"><span data-stu-id="4e916-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="4e916-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4e916-131">-KeyId</span></span>
<span data-ttu-id="4e916-132">Specifica la chiave delle credenziali da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4e916-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="4e916-133">Gli ID chiave per l'applicazione possono essere ottenuti usando il cmdlet Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="4e916-133">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="4e916-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4e916-134">-ObjectId</span></span>
<span data-ttu-id="4e916-135">ID oggetto dell'applicazione per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="4e916-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e916-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e916-136">-PassThru</span></span>
<span data-ttu-id="4e916-137">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="4e916-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4e916-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e916-138">-Confirm</span></span>
<span data-ttu-id="4e916-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e916-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e916-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e916-140">-WhatIf</span></span>
<span data-ttu-id="4e916-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e916-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e916-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e916-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e916-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e916-143">CommonParameters</span></span>
<span data-ttu-id="4e916-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e916-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e916-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e916-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e916-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e916-146">INPUTS</span></span>

### <span data-ttu-id="4e916-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="4e916-147">System.Guid</span></span>

### <span data-ttu-id="4e916-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4e916-148">System.String</span></span>

### <span data-ttu-id="4e916-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4e916-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="4e916-150">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e916-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="4e916-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e916-151">OUTPUTS</span></span>

### <span data-ttu-id="4e916-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e916-152">System.Boolean</span></span>

## <span data-ttu-id="4e916-153">Note</span><span class="sxs-lookup"><span data-stu-id="4e916-153">NOTES</span></span>

## <span data-ttu-id="4e916-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e916-154">RELATED LINKS</span></span>

[<span data-ttu-id="4e916-155">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4e916-155">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="4e916-156">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4e916-156">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="4e916-157">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4e916-157">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
