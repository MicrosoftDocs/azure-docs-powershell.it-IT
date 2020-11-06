---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520392"
---
# <span data-ttu-id="3306e-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3306e-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="3306e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3306e-102">SYNOPSIS</span></span>
<span data-ttu-id="3306e-103">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="3306e-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3306e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3306e-104">SYNTAX</span></span>

### <span data-ttu-id="3306e-105">SpObjectIdWithDisplayNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3306e-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3306e-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3306e-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3306e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3306e-107">DESCRIPTION</span></span>
<span data-ttu-id="3306e-108">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="3306e-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="3306e-109">Per aggiornare le credenziali associate all'entità di servizio, usare New-AzureRmADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3306e-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="3306e-110">Per aggiornare le proprietà associate all'applicazione sottostante, usare Set-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3306e-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="3306e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3306e-111">EXAMPLES</span></span>

### <span data-ttu-id="3306e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3306e-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="3306e-113">Aggiorna il nome visualizzato per l'entità servizio con l'ID oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="3306e-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="3306e-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3306e-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="3306e-115">Aggiorna il nome visualizzato per l'entità servizio con il nome dell'entità servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="3306e-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="3306e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3306e-116">PARAMETERS</span></span>

### <span data-ttu-id="3306e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3306e-117">-DefaultProfile</span></span>
<span data-ttu-id="3306e-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3306e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3306e-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3306e-119">-DisplayName</span></span>
<span data-ttu-id="3306e-120">Nuovo nome visualizzato per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3306e-120">New display name for the service principal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3306e-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3306e-121">-ObjectId</span></span>
<span data-ttu-id="3306e-122">ID oggetto dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="3306e-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3306e-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3306e-123">-ServicePrincipalName</span></span>
<span data-ttu-id="3306e-124">Nome SPN dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="3306e-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3306e-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3306e-125">-Confirm</span></span>
<span data-ttu-id="3306e-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3306e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3306e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3306e-127">-WhatIf</span></span>
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

### <span data-ttu-id="3306e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3306e-128">CommonParameters</span></span>
<span data-ttu-id="3306e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3306e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3306e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3306e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3306e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3306e-131">INPUTS</span></span>

### <span data-ttu-id="3306e-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3306e-132">None</span></span>
<span data-ttu-id="3306e-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3306e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3306e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3306e-134">OUTPUTS</span></span>

## <span data-ttu-id="3306e-135">Note</span><span class="sxs-lookup"><span data-stu-id="3306e-135">NOTES</span></span>

## <span data-ttu-id="3306e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3306e-136">RELATED LINKS</span></span>

[<span data-ttu-id="3306e-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3306e-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3306e-138">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3306e-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3306e-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3306e-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3306e-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3306e-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="3306e-141">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3306e-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="3306e-142">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3306e-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

