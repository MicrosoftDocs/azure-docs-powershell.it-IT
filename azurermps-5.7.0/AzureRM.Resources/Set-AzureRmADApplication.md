---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520396"
---
# <span data-ttu-id="887c4-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="887c4-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="887c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="887c4-102">SYNOPSIS</span></span>
<span data-ttu-id="887c4-103">Aggiorna un'applicazione di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="887c4-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="887c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="887c4-104">SYNTAX</span></span>

### <span data-ttu-id="887c4-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="887c4-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="887c4-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="887c4-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="887c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="887c4-107">DESCRIPTION</span></span>
<span data-ttu-id="887c4-108">Aggiorna un'applicazione di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="887c4-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="887c4-109">Per aggiornare le credenziali associate a questa applicazione, utilizzare New-AzureRmADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="887c4-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="887c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="887c4-110">EXAMPLES</span></span>

### <span data-ttu-id="887c4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="887c4-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="887c4-112">Aggiorna le proprietà di un'applicazione di Azure Active Directory esistente con objectId "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="887c4-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="887c4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="887c4-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="887c4-114">Aggiorna il nome visualizzato di un'applicazione di Azure Active Directory esistente con objectId "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="887c4-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="887c4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="887c4-115">PARAMETERS</span></span>

### <span data-ttu-id="887c4-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="887c4-116">-ApplicationId</span></span>
<span data-ttu-id="887c4-117">ID dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="887c4-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c4-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="887c4-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="887c4-119">Valore che specifica se l'applicazione viene aggiornata per essere un singolo tenant o un multi-tenant.</span><span class="sxs-lookup"><span data-stu-id="887c4-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887c4-120">-DefaultProfile</span></span>
<span data-ttu-id="887c4-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="887c4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="887c4-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="887c4-122">-DisplayName</span></span>
<span data-ttu-id="887c4-123">Nuovo nome visualizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="887c4-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c4-124">-Home page</span><span class="sxs-lookup"><span data-stu-id="887c4-124">-HomePage</span></span>
<span data-ttu-id="887c4-125">Nuovo URL della Home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="887c4-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c4-126">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="887c4-126">-IdentifierUris</span></span>
<span data-ttu-id="887c4-127">Nuovi URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="887c4-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c4-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="887c4-128">-ObjectId</span></span>
<span data-ttu-id="887c4-129">ID oggetto dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="887c4-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c4-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="887c4-130">-ReplyUrls</span></span>
<span data-ttu-id="887c4-131">Nuovi URL di risposta per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="887c4-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="887c4-132">-Confirm</span></span>
<span data-ttu-id="887c4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="887c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="887c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="887c4-134">-WhatIf</span></span>
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

### <span data-ttu-id="887c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887c4-135">CommonParameters</span></span>
<span data-ttu-id="887c4-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887c4-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="887c4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887c4-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="887c4-138">INPUTS</span></span>

### <span data-ttu-id="887c4-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="887c4-139">None</span></span>
<span data-ttu-id="887c4-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="887c4-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="887c4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="887c4-141">OUTPUTS</span></span>

### <span data-ttu-id="887c4-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="887c4-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="887c4-143">Note</span><span class="sxs-lookup"><span data-stu-id="887c4-143">NOTES</span></span>

## <span data-ttu-id="887c4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="887c4-144">RELATED LINKS</span></span>

[<span data-ttu-id="887c4-145">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="887c4-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="887c4-146">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="887c4-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="887c4-147">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="887c4-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="887c4-148">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="887c4-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="887c4-149">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="887c4-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="887c4-150">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="887c4-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

