---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: 705deeb8e9b248b480bd2a28662cc7e968f8c228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509403"
---
# <span data-ttu-id="e1ce3-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e1ce3-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="e1ce3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ce3-103">Imposta i dettagli dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ce3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1ce3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ce3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ce3-106">Il cmdlet **set-AzureRmApiManagementUser** imposta i dettagli utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="e1ce3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ce3-108">Esempio 1: modificare la password di un utente, l'indirizzo di posta elettronica e lo stato</span><span class="sxs-lookup"><span data-stu-id="e1ce3-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="e1ce3-109">Questo comando imposta una nuova password utente e un indirizzo di posta elettronica e blocca l'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="e1ce3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="e1ce3-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e1ce3-111">-Context</span></span>
<span data-ttu-id="e1ce3-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e1ce3-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e1ce3-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e1ce3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ce3-114">-DefaultProfile</span></span>
<span data-ttu-id="e1ce3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ce3-116">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="e1ce3-116">-Email</span></span>
<span data-ttu-id="e1ce3-117">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="e1ce3-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e1ce3-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e1ce3-119">-FirstName</span></span>
<span data-ttu-id="e1ce3-120">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="e1ce3-121">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="e1ce3-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="e1ce3-122">-LastName</span></span>
<span data-ttu-id="e1ce3-123">Specifica il cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="e1ce3-124">Questo parametro deve essere di lunghezza da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="e1ce3-125">-Nota</span><span class="sxs-lookup"><span data-stu-id="e1ce3-125">-Note</span></span>
<span data-ttu-id="e1ce3-126">Specifica una nota relativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-126">Specifies a note about the user.</span></span>
<span data-ttu-id="e1ce3-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-127">This parameter is optional.</span></span>
<span data-ttu-id="e1ce3-128">Il valore predefinito di questo parametro è $null.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="e1ce3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1ce3-129">-PassThru</span></span>
<span data-ttu-id="e1ce3-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="e1ce3-130">passthru</span></span>

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

### <span data-ttu-id="e1ce3-131">-Password</span><span class="sxs-lookup"><span data-stu-id="e1ce3-131">-Password</span></span>
<span data-ttu-id="e1ce3-132">Specifica la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-132">Specifies the user password.</span></span>
<span data-ttu-id="e1ce3-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce3-134">-Stato</span><span class="sxs-lookup"><span data-stu-id="e1ce3-134">-State</span></span>
<span data-ttu-id="e1ce3-135">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-135">Specifies the user state.</span></span>
<span data-ttu-id="e1ce3-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-136">This parameter is optional.</span></span>
<span data-ttu-id="e1ce3-137">Il valore predefinito è attivo.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce3-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="e1ce3-138">-UserId</span></span>
<span data-ttu-id="e1ce3-139">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-139">Specifies the user ID.</span></span>
<span data-ttu-id="e1ce3-140">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-140">This parameter is required.</span></span>

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

### <span data-ttu-id="e1ce3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ce3-141">CommonParameters</span></span>
<span data-ttu-id="e1ce3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ce3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ce3-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ce3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ce3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1ce3-144">INPUTS</span></span>

### <span data-ttu-id="e1ce3-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1ce3-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1ce3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ce3-146">System.String</span></span>

### <span data-ttu-id="e1ce3-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e1ce3-147">System.Security.SecureString</span></span>

### <span data-ttu-id="e1ce3-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="e1ce3-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="e1ce3-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1ce3-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1ce3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1ce3-150">OUTPUTS</span></span>

### <span data-ttu-id="e1ce3-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e1ce3-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="e1ce3-152">Note</span><span class="sxs-lookup"><span data-stu-id="e1ce3-152">NOTES</span></span>

## <span data-ttu-id="e1ce3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1ce3-153">RELATED LINKS</span></span>

[<span data-ttu-id="e1ce3-154">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e1ce3-154">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="e1ce3-155">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e1ce3-155">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="e1ce3-156">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e1ce3-156">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


