---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688241"
---
# <span data-ttu-id="7f3ad-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7f3ad-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="7f3ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3ad-103">Aggiorna un'applicazione di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f3ad-104">SYNTAX</span></span>

### <span data-ttu-id="7f3ad-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f3ad-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3ad-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f3ad-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f3ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f3ad-107">DESCRIPTION</span></span>
<span data-ttu-id="7f3ad-108">Aggiorna un'applicazione di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="7f3ad-109">Per aggiornare le credenziali associate a questa applicazione, utilizzare New-AzureRmADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="7f3ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f3ad-110">EXAMPLES</span></span>

### <span data-ttu-id="7f3ad-111">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f3ad-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="7f3ad-112">Aggiorna le proprietà di un'applicazione di Azure Active Directory esistente con objectId "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="7f3ad-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="7f3ad-113">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f3ad-113">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="7f3ad-114">Aggiorna il nome visualizzato di un'applicazione di Azure Active Directory esistente con objectId "fb7b3405-CA44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="7f3ad-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="7f3ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f3ad-115">PARAMETERS</span></span>

### <span data-ttu-id="7f3ad-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7f3ad-116">-ApplicationId</span></span>
<span data-ttu-id="7f3ad-117">ID dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-117">The id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ad-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="7f3ad-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="7f3ad-119">Valore che specifica se l'applicazione viene aggiornata per essere un singolo tenant o un multi-tenant.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ad-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7f3ad-120">-DisplayName</span></span>
<span data-ttu-id="7f3ad-121">Nuovo nome visualizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-121">New Display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ad-122">-Home page</span><span class="sxs-lookup"><span data-stu-id="7f3ad-122">-HomePage</span></span>
<span data-ttu-id="7f3ad-123">Nuovo URL della Home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-123">New URL of the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ad-124">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="7f3ad-124">-IdentifierUris</span></span>
<span data-ttu-id="7f3ad-125">Nuovi URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-125">New URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ad-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7f3ad-126">-ObjectId</span></span>
<span data-ttu-id="7f3ad-127">ID oggetto dell'applicazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-127">The object id of the application to update.</span></span>

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

### <span data-ttu-id="7f3ad-128">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="7f3ad-128">-ReplyUrls</span></span>
<span data-ttu-id="7f3ad-129">Nuovi URL di risposta per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-129">New reply urls for the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3ad-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f3ad-130">-Confirm</span></span>
<span data-ttu-id="7f3ad-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f3ad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f3ad-132">-WhatIf</span></span>
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

### <span data-ttu-id="7f3ad-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3ad-133">-DefaultProfile</span></span>
<span data-ttu-id="7f3ad-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f3ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3ad-135">CommonParameters</span></span>
<span data-ttu-id="7f3ad-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3ad-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3ad-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3ad-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f3ad-138">INPUTS</span></span>

## <span data-ttu-id="7f3ad-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f3ad-139">OUTPUTS</span></span>

### <span data-ttu-id="7f3ad-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7f3ad-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7f3ad-141">Note</span><span class="sxs-lookup"><span data-stu-id="7f3ad-141">NOTES</span></span>

## <span data-ttu-id="7f3ad-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f3ad-142">RELATED LINKS</span></span>

[<span data-ttu-id="7f3ad-143">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7f3ad-143">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="7f3ad-144">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7f3ad-144">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="7f3ad-145">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7f3ad-145">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="7f3ad-146">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f3ad-146">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7f3ad-147">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f3ad-147">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="7f3ad-148">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7f3ad-148">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

