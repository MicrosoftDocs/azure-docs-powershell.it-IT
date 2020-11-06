---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 0cfcb2713eaac255f625b09c0ba81883242f48aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509651"
---
# <span data-ttu-id="7818d-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7818d-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="7818d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7818d-102">SYNOPSIS</span></span>
<span data-ttu-id="7818d-103">Rimuove una credenziale da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7818d-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7818d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7818d-104">SYNTAX</span></span>

### <span data-ttu-id="7818d-105">ApplicationObjectIdWithKeyIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7818d-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7818d-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="7818d-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7818d-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7818d-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7818d-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="7818d-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7818d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7818d-109">DESCRIPTION</span></span>
<span data-ttu-id="7818d-110">Il cmdlet Remove-AzureRmADAppCredential può essere usato per rimuovere una chiave di credenziale da un'applicazione in caso di compromissione o come parte della scadenza del rollover della chiave di credenziale.</span><span class="sxs-lookup"><span data-stu-id="7818d-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7818d-111">L'applicazione viene identificata fornendo l'ID oggetto o l'AppId.</span><span class="sxs-lookup"><span data-stu-id="7818d-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="7818d-112">Le credenziali da rimuovere vengono identificate dall'ID chiave se una singola credenziale deve essere rimossa o con un interruttore "tutti" per eliminare tutte le credenziali associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7818d-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="7818d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7818d-113">EXAMPLES</span></span>

### <span data-ttu-id="7818d-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7818d-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7818d-115">Questo comando rimuove una chiave di credenziale da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7818d-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="7818d-116">In questo esempio, la chiave con ID "9044423a-60A3-45AC-9ab1-09534157ebb" verrà rimossa dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7818d-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="7818d-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7818d-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="7818d-118">Questo comando rimuove una chiave di credenziale da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7818d-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="7818d-119">In questo esempio tutte le credenziali verranno rimosse dall'applicazione associata al applicationId "4589cd6b-3D79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="7818d-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="7818d-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7818d-120">PARAMETERS</span></span>

### <span data-ttu-id="7818d-121">-Tutti</span><span class="sxs-lookup"><span data-stu-id="7818d-121">-All</span></span>
<span data-ttu-id="7818d-122">Passare a rimuovere tutte le credenziali associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7818d-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7818d-123">-ApplicationId</span></span>
<span data-ttu-id="7818d-124">ID dell'applicazione per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7818d-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7818d-125">-DefaultProfile</span></span>
<span data-ttu-id="7818d-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7818d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7818d-127">-Force</span></span>
<span data-ttu-id="7818d-128">Passare a eliminare le credenziali senza conferma.</span><span class="sxs-lookup"><span data-stu-id="7818d-128">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-129">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7818d-129">-KeyId</span></span>
<span data-ttu-id="7818d-130">Specifica la chiave delle credenziali da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7818d-130">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7818d-131">Gli ID chiave per l'applicazione possono essere ottenuti usando il cmdlet Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="7818d-131">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7818d-132">-ObjectId</span></span>
<span data-ttu-id="7818d-133">ID oggetto dell'applicazione per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7818d-133">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7818d-134">-Confirm</span></span>
<span data-ttu-id="7818d-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7818d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7818d-136">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7818d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7818d-137">CommonParameters</span></span>
<span data-ttu-id="7818d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7818d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7818d-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7818d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7818d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7818d-140">INPUTS</span></span>

### <span data-ttu-id="7818d-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7818d-141">None</span></span>
<span data-ttu-id="7818d-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7818d-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7818d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7818d-143">OUTPUTS</span></span>

## <span data-ttu-id="7818d-144">Note</span><span class="sxs-lookup"><span data-stu-id="7818d-144">NOTES</span></span>

## <span data-ttu-id="7818d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7818d-145">RELATED LINKS</span></span>

[<span data-ttu-id="7818d-146">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7818d-146">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="7818d-147">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7818d-147">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7818d-148">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7818d-148">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
