---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518432"
---
# <span data-ttu-id="18549-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="18549-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="18549-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18549-102">SYNOPSIS</span></span>
<span data-ttu-id="18549-103">Registra un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="18549-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18549-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18549-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18549-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18549-105">DESCRIPTION</span></span>
<span data-ttu-id="18549-106">Il cmdlet **New-AzureRmApiManagementUser** registra un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="18549-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="18549-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18549-107">EXAMPLES</span></span>

### <span data-ttu-id="18549-108">Esempio 1: registrare un nuovo utente</span><span class="sxs-lookup"><span data-stu-id="18549-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="18549-109">Questo comando registra un nuovo utente di nome Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="18549-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="18549-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18549-110">PARAMETERS</span></span>

### <span data-ttu-id="18549-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="18549-111">-Context</span></span>
<span data-ttu-id="18549-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="18549-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18549-113">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="18549-113">-Email</span></span>
<span data-ttu-id="18549-114">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18549-114">Specifies the email address of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18549-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="18549-115">-FirstName</span></span>
<span data-ttu-id="18549-116">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18549-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="18549-117">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="18549-117">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18549-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="18549-118">-LastName</span></span>
<span data-ttu-id="18549-119">Specifica il cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18549-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="18549-120">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="18549-120">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18549-121">-Nota</span><span class="sxs-lookup"><span data-stu-id="18549-121">-Note</span></span>
<span data-ttu-id="18549-122">Specifica una nota relativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="18549-122">Specifies a note about the user.</span></span>
<span data-ttu-id="18549-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18549-123">This parameter is optional.</span></span>
<span data-ttu-id="18549-124">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="18549-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="18549-125">-Password</span><span class="sxs-lookup"><span data-stu-id="18549-125">-Password</span></span>
<span data-ttu-id="18549-126">Specifica la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18549-126">Specifies the user password.</span></span>
<span data-ttu-id="18549-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="18549-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18549-128">-Stato</span><span class="sxs-lookup"><span data-stu-id="18549-128">-State</span></span>
<span data-ttu-id="18549-129">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18549-129">Specifies the user state.</span></span>
<span data-ttu-id="18549-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18549-130">This parameter is optional.</span></span>
<span data-ttu-id="18549-131">Il valore predefinito di questo parametro è $Null.</span><span class="sxs-lookup"><span data-stu-id="18549-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18549-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="18549-132">-UserId</span></span>
<span data-ttu-id="18549-133">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="18549-133">Specifies the user ID.</span></span>
<span data-ttu-id="18549-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18549-134">This parameter is optional.</span></span>
<span data-ttu-id="18549-135">Se questo parametro non viene specificato, questo cmdlet genera un ID utente.</span><span class="sxs-lookup"><span data-stu-id="18549-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="18549-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18549-136">-DefaultProfile</span></span>
<span data-ttu-id="18549-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18549-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18549-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18549-138">CommonParameters</span></span>
<span data-ttu-id="18549-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18549-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18549-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18549-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18549-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18549-141">INPUTS</span></span>

## <span data-ttu-id="18549-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18549-142">OUTPUTS</span></span>

### <span data-ttu-id="18549-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="18549-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="18549-144">Note</span><span class="sxs-lookup"><span data-stu-id="18549-144">NOTES</span></span>

## <span data-ttu-id="18549-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18549-145">RELATED LINKS</span></span>

[<span data-ttu-id="18549-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="18549-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="18549-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="18549-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


