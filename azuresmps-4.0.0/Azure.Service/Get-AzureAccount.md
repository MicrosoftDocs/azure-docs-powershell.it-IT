---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023634"
---
# <span data-ttu-id="47112-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="47112-101">Get-AzureAccount</span></span>

## <span data-ttu-id="47112-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47112-102">SYNOPSIS</span></span>
<span data-ttu-id="47112-103">Ottiene gli account Azure disponibili per Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="47112-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="47112-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47112-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47112-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47112-105">DESCRIPTION</span></span>
<span data-ttu-id="47112-106">Il cmdlet **Get-AzureAccount** ottiene gli account di Azure disponibili per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="47112-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="47112-107">Per rendere gli account disponibili per Windows PowerShell, usare i cmdlet **Add-AzureAccount** o **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="47112-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="47112-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47112-108">EXAMPLES</span></span>

### <span data-ttu-id="47112-109">Esempio 1: ottenere tutti gli account</span><span class="sxs-lookup"><span data-stu-id="47112-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="47112-110">Questo comando consente di ottenere tutti gli account associati all'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="47112-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="47112-111">Esempio 2: ottenere un account per nome</span><span class="sxs-lookup"><span data-stu-id="47112-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="47112-112">Questo comando ottiene l'account ContosoAdmin.</span><span class="sxs-lookup"><span data-stu-id="47112-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="47112-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47112-113">PARAMETERS</span></span>

### <span data-ttu-id="47112-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="47112-114">-Name</span></span>
<span data-ttu-id="47112-115">Ottiene solo l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="47112-115">Gets only the specified account.</span></span>
<span data-ttu-id="47112-116">L'impostazione predefinita è tutti gli account disponibili per Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="47112-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="47112-117">Immettere il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="47112-117">Enter the account name.</span></span>
<span data-ttu-id="47112-118">Il valore **Name** fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="47112-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="47112-119">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="47112-119">Wildcards are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47112-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="47112-120">-Profile</span></span>
<span data-ttu-id="47112-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47112-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="47112-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="47112-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47112-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47112-123">CommonParameters</span></span>
<span data-ttu-id="47112-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47112-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47112-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47112-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47112-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47112-126">INPUTS</span></span>

### <span data-ttu-id="47112-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47112-127">None</span></span>
<span data-ttu-id="47112-128">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47112-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="47112-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47112-129">OUTPUTS</span></span>

### <span data-ttu-id="47112-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47112-130">None</span></span>
<span data-ttu-id="47112-131">Questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="47112-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="47112-132">Note</span><span class="sxs-lookup"><span data-stu-id="47112-132">NOTES</span></span>

## <span data-ttu-id="47112-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47112-133">RELATED LINKS</span></span>

[<span data-ttu-id="47112-134">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="47112-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="47112-135">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="47112-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="47112-136">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="47112-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="47112-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="47112-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


