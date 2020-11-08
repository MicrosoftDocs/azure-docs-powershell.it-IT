---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029683"
---
# <span data-ttu-id="b2b72-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b2b72-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="b2b72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2b72-102">SYNOPSIS</span></span>

<span data-ttu-id="b2b72-103">Crea una credenziale nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="b2b72-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="b2b72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2b72-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2b72-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2b72-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b2b72-106">Il cmdlet **New-AzureAutomationCredential** crea una credenziale come oggetto **PSCredential** in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b2b72-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="b2b72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2b72-107">EXAMPLES</span></span>

### <span data-ttu-id="b2b72-108">Esempio 1: creare una credenziale</span><span class="sxs-lookup"><span data-stu-id="b2b72-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="b2b72-109">Questi comandi creano una credenziale denominata Credential.</span><span class="sxs-lookup"><span data-stu-id="b2b72-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="b2b72-110">Viene prima creato un oggetto Credential che include un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="b2b72-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="b2b72-111">Questo viene quindi usato nell'ultimo comando per creare le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="b2b72-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="b2b72-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2b72-112">PARAMETERS</span></span>

### <span data-ttu-id="b2b72-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2b72-113">-AutomationAccountName</span></span>
<span data-ttu-id="b2b72-114">Specifica il nome dell'account di automazione in cui verranno archiviate le credenziali.</span><span class="sxs-lookup"><span data-stu-id="b2b72-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="b2b72-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2b72-115">-Description</span></span>
<span data-ttu-id="b2b72-116">Specifica una descrizione per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="b2b72-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="b2b72-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2b72-117">-Name</span></span>
<span data-ttu-id="b2b72-118">Specifica un nome per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="b2b72-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="b2b72-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="b2b72-119">-Profile</span></span>
<span data-ttu-id="b2b72-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b72-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2b72-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b2b72-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b72-122">-Valore</span><span class="sxs-lookup"><span data-stu-id="b2b72-122">-Value</span></span>
<span data-ttu-id="b2b72-123">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="b2b72-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b72-124">CommonParameters</span></span>
<span data-ttu-id="b2b72-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b72-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b72-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b72-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2b72-127">INPUTS</span></span>

## <span data-ttu-id="b2b72-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2b72-128">OUTPUTS</span></span>

### <span data-ttu-id="b2b72-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="b2b72-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="b2b72-130">Note</span><span class="sxs-lookup"><span data-stu-id="b2b72-130">NOTES</span></span>

## <span data-ttu-id="b2b72-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2b72-131">RELATED LINKS</span></span>

[<span data-ttu-id="b2b72-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b2b72-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="b2b72-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b2b72-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="b2b72-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b2b72-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


