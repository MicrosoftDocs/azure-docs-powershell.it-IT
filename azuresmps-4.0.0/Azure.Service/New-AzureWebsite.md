---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110479"
---
# <span data-ttu-id="97f47-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="97f47-101">New-AzureWebsite</span></span>

## <span data-ttu-id="97f47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97f47-102">SYNOPSIS</span></span>
<span data-ttu-id="97f47-103">Creare un nuovo sito Web per l'esecuzione in Azure.</span><span class="sxs-lookup"><span data-stu-id="97f47-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="97f47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97f47-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97f47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97f47-105">DESCRIPTION</span></span>
<span data-ttu-id="97f47-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97f47-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="97f47-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="97f47-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="97f47-108">Il cmdlet crea un nuovo sito Web per l'esecuzione in Azure e si prepara per la distribuzione tramite GitHub.</span><span class="sxs-lookup"><span data-stu-id="97f47-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="97f47-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97f47-109">EXAMPLES</span></span>

### <span data-ttu-id="97f47-110">Esempio 1: creare un nuovo sito Web con git</span><span class="sxs-lookup"><span data-stu-id="97f47-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="97f47-111">Questo esempio crea un nuovo sito Web in Azure e un repository git locale da usare per la distribuzione di file nel nuovo sito Web.</span><span class="sxs-lookup"><span data-stu-id="97f47-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="97f47-112">Esempio 2: creare un sito Web integrato con GitHub</span><span class="sxs-lookup"><span data-stu-id="97f47-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="97f47-113">Questo esempio crea un nuovo sito Web collegato a un repository di GitHub denominato account/repo.</span><span class="sxs-lookup"><span data-stu-id="97f47-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="97f47-114">I commit al repository GitHub vengono spostati nel sito Web in Azure.</span><span class="sxs-lookup"><span data-stu-id="97f47-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="97f47-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97f47-115">PARAMETERS</span></span>

### <span data-ttu-id="97f47-116">-Git</span><span class="sxs-lookup"><span data-stu-id="97f47-116">-Git</span></span>
<span data-ttu-id="97f47-117">Configura un repository git locale e lo collega al sito Web.</span><span class="sxs-lookup"><span data-stu-id="97f47-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="97f47-118">Se specificato, questo parametro configura un repository git nella directory locale e aggiunge un repository remoto denominato "Azure" che si collega al sito Web in Azure.</span><span class="sxs-lookup"><span data-stu-id="97f47-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f47-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="97f47-119">-GitHub</span></span>
<span data-ttu-id="97f47-120">Indica che questo cmdlet collega il nuovo sito Web a un repository di GitHub esistente.</span><span class="sxs-lookup"><span data-stu-id="97f47-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="97f47-121">I commit al repository Giuthub vengono spostati nel sito Web in Azure.</span><span class="sxs-lookup"><span data-stu-id="97f47-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f47-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="97f47-122">-GitHubCredentials</span></span>
<span data-ttu-id="97f47-123">Specifica le credenziali di nome utente e password per la connessione a GitHub.</span><span class="sxs-lookup"><span data-stu-id="97f47-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f47-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="97f47-124">-GitHubRepository</span></span>
<span data-ttu-id="97f47-125">Specifica il nome completo del repository GitHub da collegare a questo sito Web.</span><span class="sxs-lookup"><span data-stu-id="97f47-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="97f47-126">Ad esempio, `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="97f47-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="97f47-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="97f47-127">-Hostname</span></span>
<span data-ttu-id="97f47-128">Specifica un nome host alternativo per il nuovo sito Web.</span><span class="sxs-lookup"><span data-stu-id="97f47-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="97f47-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="97f47-129">-Location</span></span>
<span data-ttu-id="97f47-130">Specifica la posizione del centro dati in cui si vuole distribuire il sito Web.</span><span class="sxs-lookup"><span data-stu-id="97f47-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="97f47-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="97f47-131">-Name</span></span>
<span data-ttu-id="97f47-132">Specifica un nome per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="97f47-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="97f47-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="97f47-133">-Profile</span></span>
<span data-ttu-id="97f47-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97f47-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97f47-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="97f47-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97f47-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="97f47-136">-PublishingUsername</span></span>
<span data-ttu-id="97f47-137">Specifica il nome utente specificato in Azure Portal per la distribuzione git.</span><span class="sxs-lookup"><span data-stu-id="97f47-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="97f47-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="97f47-138">-Slot</span></span>
<span data-ttu-id="97f47-139">Specifica un nome di slot per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="97f47-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="97f47-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f47-140">CommonParameters</span></span>
<span data-ttu-id="97f47-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f47-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f47-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f47-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f47-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97f47-143">INPUTS</span></span>

## <span data-ttu-id="97f47-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97f47-144">OUTPUTS</span></span>

## <span data-ttu-id="97f47-145">Note</span><span class="sxs-lookup"><span data-stu-id="97f47-145">NOTES</span></span>

## <span data-ttu-id="97f47-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97f47-146">RELATED LINKS</span></span>

[<span data-ttu-id="97f47-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="97f47-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


