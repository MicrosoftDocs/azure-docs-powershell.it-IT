---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: a70cc953da853fd07dcee835f5a97a0efd2f6406
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022126"
---
# <span data-ttu-id="74145-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74145-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="74145-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74145-102">SYNOPSIS</span></span>
<span data-ttu-id="74145-103">Imposta i dettagli dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-103">Sets user details.</span></span>

## <span data-ttu-id="74145-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74145-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74145-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74145-105">DESCRIPTION</span></span>
<span data-ttu-id="74145-106">Il cmdlet **set-AzApiManagementUser** imposta i dettagli utente.</span><span class="sxs-lookup"><span data-stu-id="74145-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="74145-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74145-107">EXAMPLES</span></span>

### <span data-ttu-id="74145-108">Esempio 1: modificare la password di un utente, l'indirizzo di posta elettronica e lo stato</span><span class="sxs-lookup"><span data-stu-id="74145-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="74145-109">Questo comando imposta una nuova password utente e un indirizzo di posta elettronica e blocca l'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="74145-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74145-110">PARAMETERS</span></span>

### <span data-ttu-id="74145-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="74145-111">-Context</span></span>
<span data-ttu-id="74145-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="74145-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="74145-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="74145-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74145-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74145-114">-DefaultProfile</span></span>
<span data-ttu-id="74145-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74145-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74145-116">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="74145-116">-Email</span></span>
<span data-ttu-id="74145-117">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="74145-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74145-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="74145-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="74145-119">-FirstName</span></span>
<span data-ttu-id="74145-120">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="74145-121">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="74145-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="74145-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="74145-122">-LastName</span></span>
<span data-ttu-id="74145-123">Specifica il cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="74145-124">Questo parametro deve essere di lunghezza da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="74145-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="74145-125">-Nota</span><span class="sxs-lookup"><span data-stu-id="74145-125">-Note</span></span>
<span data-ttu-id="74145-126">Specifica una nota relativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-126">Specifies a note about the user.</span></span>
<span data-ttu-id="74145-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74145-127">This parameter is optional.</span></span>
<span data-ttu-id="74145-128">Il valore predefinito di questo parametro è $null.</span><span class="sxs-lookup"><span data-stu-id="74145-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="74145-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74145-129">-PassThru</span></span>
<span data-ttu-id="74145-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="74145-130">passthru</span></span>

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

### <span data-ttu-id="74145-131">-Password</span><span class="sxs-lookup"><span data-stu-id="74145-131">-Password</span></span>
<span data-ttu-id="74145-132">Specifica la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-132">Specifies the user password.</span></span>
<span data-ttu-id="74145-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74145-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="74145-134">-Stato</span><span class="sxs-lookup"><span data-stu-id="74145-134">-State</span></span>
<span data-ttu-id="74145-135">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74145-135">Specifies the user state.</span></span>
<span data-ttu-id="74145-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74145-136">This parameter is optional.</span></span>
<span data-ttu-id="74145-137">Il valore predefinito è attivo.</span><span class="sxs-lookup"><span data-stu-id="74145-137">The default value is Active.</span></span>

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

### <span data-ttu-id="74145-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="74145-138">-UserId</span></span>
<span data-ttu-id="74145-139">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="74145-139">Specifies the user ID.</span></span>
<span data-ttu-id="74145-140">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="74145-140">This parameter is required.</span></span>

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

### <span data-ttu-id="74145-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74145-141">-Confirm</span></span>
<span data-ttu-id="74145-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74145-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74145-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74145-143">-WhatIf</span></span>
<span data-ttu-id="74145-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74145-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74145-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74145-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74145-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74145-146">CommonParameters</span></span>
<span data-ttu-id="74145-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74145-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74145-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74145-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74145-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74145-149">INPUTS</span></span>

### <span data-ttu-id="74145-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="74145-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="74145-151">System. String</span><span class="sxs-lookup"><span data-stu-id="74145-151">System.String</span></span>

### <span data-ttu-id="74145-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="74145-152">System.Security.SecureString</span></span>

### <span data-ttu-id="74145-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="74145-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="74145-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74145-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74145-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74145-155">OUTPUTS</span></span>

### <span data-ttu-id="74145-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74145-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="74145-157">Note</span><span class="sxs-lookup"><span data-stu-id="74145-157">NOTES</span></span>

## <span data-ttu-id="74145-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74145-158">RELATED LINKS</span></span>

[<span data-ttu-id="74145-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74145-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="74145-160">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74145-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="74145-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74145-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


