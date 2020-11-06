---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508780"
---
# <span data-ttu-id="172f0-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="172f0-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="172f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="172f0-102">SYNOPSIS</span></span>
<span data-ttu-id="172f0-103">Imposta i dettagli dell'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="172f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="172f0-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="172f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="172f0-105">DESCRIPTION</span></span>
<span data-ttu-id="172f0-106">Il cmdlet **set-AzureRmApiManagementUser** imposta i dettagli utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="172f0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="172f0-107">EXAMPLES</span></span>

### <span data-ttu-id="172f0-108">Esempio 1: modificare la password di un utente, l'indirizzo di posta elettronica e lo stato</span><span class="sxs-lookup"><span data-stu-id="172f0-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="172f0-109">Questo comando imposta una nuova password utente e un indirizzo di posta elettronica e blocca l'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="172f0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="172f0-110">PARAMETERS</span></span>

### <span data-ttu-id="172f0-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="172f0-111">-Context</span></span>
<span data-ttu-id="172f0-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="172f0-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="172f0-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="172f0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="172f0-114">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="172f0-114">-Email</span></span>
<span data-ttu-id="172f0-115">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="172f0-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="172f0-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="172f0-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="172f0-117">-FirstName</span></span>
<span data-ttu-id="172f0-118">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="172f0-119">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="172f0-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="172f0-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="172f0-120">-LastName</span></span>
<span data-ttu-id="172f0-121">Specifica il cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="172f0-122">Questo parametro deve essere di lunghezza da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="172f0-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="172f0-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="172f0-123">-Note</span></span>
<span data-ttu-id="172f0-124">Specifica una nota relativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-124">Specifies a note about the user.</span></span>
<span data-ttu-id="172f0-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="172f0-125">This parameter is optional.</span></span>
<span data-ttu-id="172f0-126">Il valore predefinito di questo parametro è $null.</span><span class="sxs-lookup"><span data-stu-id="172f0-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="172f0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="172f0-127">-PassThru</span></span>
<span data-ttu-id="172f0-128">PassThru</span><span class="sxs-lookup"><span data-stu-id="172f0-128">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="172f0-129">-Password</span><span class="sxs-lookup"><span data-stu-id="172f0-129">-Password</span></span>
<span data-ttu-id="172f0-130">Specifica la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-130">Specifies the user password.</span></span>
<span data-ttu-id="172f0-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="172f0-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="172f0-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="172f0-132">-State</span></span>
<span data-ttu-id="172f0-133">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-133">Specifies the user state.</span></span>
<span data-ttu-id="172f0-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="172f0-134">This parameter is optional.</span></span>
<span data-ttu-id="172f0-135">Il valore predefinito è attivo.</span><span class="sxs-lookup"><span data-stu-id="172f0-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="172f0-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="172f0-136">-UserId</span></span>
<span data-ttu-id="172f0-137">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="172f0-137">Specifies the user ID.</span></span>
<span data-ttu-id="172f0-138">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="172f0-138">This parameter is required.</span></span>

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

### <span data-ttu-id="172f0-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172f0-139">-DefaultProfile</span></span>
<span data-ttu-id="172f0-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="172f0-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="172f0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172f0-141">CommonParameters</span></span>
<span data-ttu-id="172f0-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172f0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172f0-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="172f0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172f0-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="172f0-144">INPUTS</span></span>

## <span data-ttu-id="172f0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="172f0-145">OUTPUTS</span></span>

### <span data-ttu-id="172f0-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="172f0-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="172f0-147">Note</span><span class="sxs-lookup"><span data-stu-id="172f0-147">NOTES</span></span>

## <span data-ttu-id="172f0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="172f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="172f0-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="172f0-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="172f0-150">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="172f0-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="172f0-151">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="172f0-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


